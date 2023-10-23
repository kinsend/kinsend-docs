# Automated Responses

Automated responses are made up of 2 components.

**First contact** - This handles all phone numbers that contact our user for the first time (they do not exist in our contact's phone book)
The flow for First Contact is as follows:

1. The trigger is the first message or phone call from a non-contact
2. A custom message is immediately sent to the non-contact which must contain an opt-in form which a user can set up in the forms and widgets page. The forms and widgets page always has at least 1 default form that is made upon account creation with name, phone and email being the default questions in the form.
3. The flow then waits 30 minutes
4. The flow does a check to see if the phone number is now associated with a contact. If it is then the flow is exited.
5. If the flow does not see the phone number associated with a contact, another custom message is sent. This message does not have to include the form if the user does not want it to. Whether the contact opts in or not, the flow is then exited

**Keyword responses** - This handles automated responses to any texts received by our user from their existing subscribers which matches the exact character sequence place in the "Rule input"

1. The trigger for these responses is whatever the user sets up to be a trigger. This trigger can be an emoji (i.e 😄), a hashtag (i.e #15Discount) or any regex response (i.e TAKE15)
2. The response will be whatever the user inputs into the "Auto Reponse" input
3. A user can tag anyone with whatever they would like based on the Keyword message they receive
4. Order of priority of the auto responses is based on the listed order. For example if I have 2 different responses for "Hello" and "TAKE15", but a subscriber sends our user "Hello TAKE15", then the subscriber should only receive the highest priority response of the 2. Regex Rules take priority over Hashtag / Emoji rules. Regex rules are prioritized by the highest level rule to the lowest level rule. Hashtag / Emoji rules are prioritized by the highest level rule to the lowest level rule.