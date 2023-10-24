# Automated Responses

[BE Test cases to implement](https://github.com/kinsend/kinsend-be/issues/170)

Automated responses comprise two main components:

---

## 1. First Contact

Handling all initial contacts from phone numbers not in the user's phone book.

- **Trigger**: First message or call from an unknown contact.
  
- **Action**:
  
  1. An immediate custom message is dispatched, always containing an opt-in form configurable in the "Forms and Widgets" page. (Note: This page defaults to having one form with fields: name, phone, and email, upon account creation.)
  2. Wait for 30 minutes.
  3. Check if the phone number has been associated with a contact.
     - If it is, exit the flow.
     - If not, send another custom message (may or may not contain the form based on user preference). Then, exit the flow regardless of opt-in status.

---

## 2. Keyword Responses

Handles automated reactions to specific sequences received from known contacts or subscribers.

- **Trigger**: Defined by the user, which can be:
  - An emoji (e.g., 😄)
  - A hashtag (e.g., #15Discount)
  - A regex pattern (e.g., TAKE15)

- **Action**:
  
  1. Send the user-defined message from the "Auto Response" field.
  2. Users have the capability to assign tags to any contact based on the received keyword message.
  
- **Priority**:

  - Rules are applied based on their listing order.
  - For conflicting triggers in a single message (e.g., "Hello TAKE15"), only the highest priority rule gets applied.
    - Regex rules > Hashtag/Emoji rules.
    - Within each category, it goes from the topmost (highest) rule to the bottommost.
