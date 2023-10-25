# Updates & SQS

The Updates feature in **Kinsend** allows you to send scheduled or immediate messages to your users. This functionality is essential for sending out bulk SMS messages or individual updates.

## Send An Update

### 1. Message Content
- Use the text input field to write the message you want to send.
- Incorporate dynamic fields using **Merge Tags**:
  - **Using Merge Tags**: Start typing with the `<` character to view a dropdown of available merge tags.
  - **Available Merge Tags**: `<fname>`, `<lname>`, `<name>`, `<mobile>`, `<email>`
  - **Selecting a Merge Tag**: Navigate using the up and down arrow keys or click on the desired merge tag with your mouse.

- **Message Counters Explained**:
  - **Left Counter (Character Counter)**: Displays the number of characters remaining in the current message segment.
  - **Right Counter (Segment Counter)**: Indicates the total number of segments your message has.
  - [Cost Implications Details](/architecture/functionality/payments.html)

### 2. Recipients
- Target a specific audience segment using the "Recipients" feature.
- **Available Segmentation Categories**:
  - **Contact Data**: Target based on specific contact attributes such as birthdays, VIP status, etc.
  - **Geographic Location**: Target based on geographic data. A future Google API integration will allow more precise targeting.
  - [**Custom Tags Details**](/developers/architecture/functionality/settings/tags-and-segments.html)
  - [**Custom Segments Details**](/developers/architecture/functionality/settings/tags-and-segments.html)

### 3. Schedule Time/Interval
- Select when the message will be sent out.
- Choose the desired frequency and set the exact date and time.

### 4. Controls
- [**Save Button**](#5-schedule-update-modal): Click this to open the schedule update modal.
- **Cancel Button**: Discard changes or the message.

### 5. Schedule Update Modal
- **Preview**: Double-check the message content for accuracy.
- **SEND TEST**: Dispatch a test message to a specific contact.
- **SCHEDULE**: Confirm and set the message to dispatch at your pre-set date and time.
