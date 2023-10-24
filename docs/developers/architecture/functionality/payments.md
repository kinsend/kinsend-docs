# Payments

## Monthly Payments:

- Minimum monthly payment from clients should be the monthly subscription

    - If (number of contacts * the rate per contact based on plan) + 
    (number of domestic message segments sent * 0.015 ) + 
    (number of international message segments * international message rates)  <
    - Monthly payment then the clients are within their monthly limits
    - International rates are calculated as Twilio rates by country * 2
    - For example: $0.2184 (Twilio rate to send to Pakistan) * 2 = $0.4368 (our rate per outbound sms segment to Pakistan)
    - Our per message domestic and various per message international rates are charged by message segment NOT by message
    - A message segment is a maximum of 160 characters
    -  For example: if a user of ours sends a message to one of their subscribers in the US with exactly 700 characters, then we will calculate that into their bill as $0.075 (5 message segments * $0.015)
    - $2 / mo / phone number
    - Make sure automations and automated responses are calculated correctly and into this monthly usage


## Updates
- Clients are charged UPFRONT for updates right before the messages are sent to avoid them canceling the next month before paying their monthly bill and them sticking us with their high       Twilio overage bill
    - For example: A client sends out an update to 95 domestic subscribers, 3 international subscribers in Pakistan, and 2 international subscribers in Mexico. The update has 2 message segments.

    The bill will be calculated as follows:

    - (95 domestic subscribers * 2 message segments * $0.015) + (3 Pakistani subscribers * 2 message segments * $0.4368) + (2 Mexican subscribers * 2 message segments * $0.103) = $3.7964 (We would charge them the rounded number of $3.80)

- If by the next billing cycle the client is still within their monthly usage limits based on their subscription then their monthly bill will be charged as their (flat fee - all upfront update payments)
    - Example monthly billing scenario:
        - Client is on a Growth plan for $249.99 which is their limit based on calculated usage
        - They have 1,000 subscribers
        - They sent 2,000 NON UPDATES domestic messages
        - They sent 2 updates within the month totaling $20 each ($40 total)
        - Non updates related usage is (1,000 subscribers * .08) + (2,000 * .015) + $40 worth of updates = $150 (which is less than their $249.99 limit)
        - So their renewal bill will be $209.99 ($249.99 - $40 worth of updates)

- If they by the next billing cycle the client is NOT within their monthly usage limits based on their subscription then their monthly bill will be charged HIGHER than their original subscription fee
    - Example monthly billing scenario:
        - Client is on a High Volume plan for $499 which is their limit based on calculated usage
        - They have 50,000 subscribers
        - They sent 100,000 NON UPDATES domestic messages
        - They sent 2 updates within the month totaling $200 each ($400 total)
        - Non updates related usage is (50,000 subscribers * .01) + (100,000 * .015) + $400 worth of updates = $2,400 (which is greater than their $499 limit)
        - So their renewal bill will be $2,000 ($2,400 - $400 worth of updates)

## Additional Notes
**Contract Plans**

- Will be billed monthly but with a 12 month minimum contract agreement
- Same 3 plans (Starter, Growth, High Volume), but at cheaper flat fees and message rates
    - Starter will be $89.99/mo with a $0.011 / message rate
    - Growth will be $224.99/mo with a $0.011 / message rate
    - High Volume will be $449.99/mo with a $0.011 / message rate
- There will need to be an automated sendgrid contract generated that is associated with this plan that will automatically be sent to the client’s email once they select a contract plan and fill out the initial form. There will need to be an event that is triggered once they have signed the contract and verified their email address to allow them to login to their respective account and pay the first month’s fee
	
**Annual Plans**

- Will be billed upfront for 12 months 
- Same 3 plans (Starter, Growth, High Volume), but at cheaper flat fees and message rates
    - Starter will be $960/yr with a $0.012 / message rate
    - Growth will be $2,400/yr with a $0.012 / message rate
    - High Volume will be $4,800/yr with a $0.012 / message rate
- All plans will still be calculated throughout each month and the user will be charged all overages every month. Monthly value limits will be as follows:
    - $80 for Starter
    - $200 for Growth
    - $400 for High Volume
- Updates will NOT be charged upfront and will just be calculated into monthly usage to determine if an overage should be charged at the end of the month or not
	
**A2P 10DLC Registration**

- Monthly plan will not begin rebilling cycle until 30 days AFTER A2P 10DLC approval
- Annual plan will not begin rebilling cycle until 365 days AFTER A2P 10DLC approval
- A2P Registration will be charged as a separate charge from initial KinSend sign up
- A2P Monthly fee will be charged as a separate charge from monthly fees / usage fees
- Starter Plan: 
    - $4 one time fee for brand registration
    - $15 one time fee for campaign
    - $1.50 / mo
- Standard Plan:
    - $44 one time fee for brand registration
    - $15 one time fee for campaign
    - $10 / mo (But could be different based on use case. We must charge the user what Twilio is charging us)
- Useful links for A2P Billing: 
    - https://support.twilio.com/hc/en-us/articles/1260803965530-What-pricing-and-fees-are-associated-with-the-A2P-10DLC-service-
    - https://support.twilio.com/hc/en-us/articles/4407882914971-Comparison-between-Starter-Low-Volume-Standard-and-Standard-registration-for-A2P-10DLC#:~:text=Campaign(s)%20%2D%20details-,Comparison%20table%20%2D%20Sole%20Proprietor%20vs.%20Standard%20A2P%2010DLC%20registration,-Sole%20Prop%C2%A0registration

