# Payments

[Payments test cases](https://github.com/kinsend/kinsend-be/issues/167)
[Subscriptions test cases](https://github.com/kinsend/kinsend-be/issues/164)

## Monthly Payments:

- Minimum monthly payment from clients should be the monthly subscription
  - If `(number of contacts * rate per contact based on plan) + (number of domestic message segments sent * 0.015 ) + (number of international message segments * international message rates)  < Monthly payment`, then the clients are within their monthly limits.
  - International rates are calculated as `Twilio rates by country * 2`
    - Example: `$0.2184` (Twilio rate to send to Pakistan) * 2 = `$0.4368` (our rate per outbound SMS segment to Pakistan)
  - Our per message domestic and various per message international rates are charged by message segment NOT by message.
  - A message segment is a maximum of 160 characters.
    - For example: if a user sends a message with 700 characters in the US, the bill is `$0.075` (5 message segments * `$0.015`)
  - `$2 / mo / phone number`
  - Ensure automations and automated responses are calculated into this monthly usage.

## Updates

- Clients are charged UPFRONT for updates right before messages are sent to avoid cancellations and us bearing their Twilio overage bill.
  - Example: An update sent to 95 domestic subscribers, 3 international in Pakistan, and 2 in Mexico with 2 message segments.
  - The bill is calculated as: `(95 * 2 * $0.015) + (3 * 2 * $0.4368) + (2 * 2 * $0.103) = $3.7964`. We charge `$3.80`.

- Monthly billing scenarios are:
  1. Within monthly usage: 
      - Client is on a Growth plan for `$249.99` with a usage calculation of `$150`. Their renewal is `$209.99` (`$249.99 - $40` from updates).
  2. Beyond monthly usage:
      - Client is on a High Volume plan for `$499` with a usage calculation of `$2,400`. Their renewal is `$2,000` (`$2,400 - $400` from updates).

## Additional Notes

### Contract Plans

- Billed monthly with a 12-month minimum contract.
- Plans:
  - Starter: `$89.99/mo` at `$0.011 / message`
  - Growth: `$224.99/mo` at `$0.011 / message`
  - High Volume: `$449.99/mo` at `$0.011 / message`
- An automated SendGrid contract is associated and sent upon selection, with an event trigger after contract signature and email verification.

### Annual Plans

- Billed upfront for 12 months.
- Plans:
  - Starter: `$960/yr` at `$0.012 / message` with `$80` monthly limit.
  - Growth: `$2,400/yr` at `$0.012 / message` with `$200` monthly limit.
  - High Volume: `$4,800/yr` at `$0.012 / message` with `$400` monthly limit.
- Updates aren't charged upfront, they're calculated into monthly usage.

### A2P 10DLC Registration

- Rebilling cycles are after A2P 10DLC approval.
- A2P registration is separate from KinSend signup.
- Starter Plan:
    - Brand registration: `$4`
    - Campaign fee: `$15`
    - Monthly fee: `$1.50`
- Standard Plan:
    - Brand registration: `$44`
    - Campaign fee: `$15`
    - Monthly fee: `$10` (Varies based on use case, charge as Twilio charges us)
- Useful links for A2P Billing: 
    - [Twilio A2P Pricing & Fees](https://support.twilio.com/hc/en-us/articles/1260803965530-What-pricing-and-fees-are-associated-with-the-A2P-10DLC-service-)
    - [Comparison between Starter and Standard A2P 10DLC registration](https://support.twilio.com/hc/en-us/articles/4407882914971-Comparison-between-Starter-Low-Volume-Standard-and-Standard-registration-for-A2P-10DLC#:~:text=Campaign(s)%20%2D%20details-,Comparison%20table%20%2D%20Sole%20Proprietor%20vs.%20Standard%20A2P%2010DLC%20registration,-Sole%20Prop%C2%A0registration)
