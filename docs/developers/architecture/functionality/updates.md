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

## Updates Yet to be Dispatched

After scheduling an update, it will be displayed prominently, notifying you of when the update is set to go out. This allows you to easily keep track of your upcoming communication.

![Updates yet to be dispatched](/assets/images/scheduled-update.png)
For example, in the provided interface:

- **Your next Update goes out in 6 days**: Provides a countdown to when the next update is due to be dispatched.
- **Hi <fname>...**: Offers a glimpse of the message content.
- **Schedule 10/31/2023 02:56 PM. to Once**: Specifies the timing and frequency of the update.

### Managing Scheduled Updates

Once an update is scheduled, users can manage their updates before they're dispatched:

- **Edit**: Click on the three dots (or "ellipsis" icon) next to the scheduled update and choose 'Edit' to modify the content, timing, or any other details. 
- **Delete**: If needed, users can select 'Delete' to remove the scheduled update from the queue. Ensure to double-check before deleting.

Reviewing and managing updates regularly ensures timely and relevant communications.

## Past Updates

The right panel provides a historical record of sent updates:

- **Message Preview**: A snippet of the update content.
- **Timestamp**: The exact date and time of the dispatched update (e.g., "10/23/2023 at 04:52 PM").
- **Frequency**: The recurrence setting of the update (e.g., "Once").

## Analytics for a Single Past Update

When you navigate to a specific past update within the KinSend platform, you are presented with detailed analytics data for that specific update. This comprehensive view provides insights into the effectiveness of the communication, allowing you to make informed decisions for future updates.

### Overview
At the top, you'll see:
- **Title of the Update**: The heading, such as "Hey <fname> testing", gives you the subject or the beginning of the message for quick identification.
- **Sent Date**: Details of when the update was dispatched, including date and time.

### Recipients
This section gives you an overview of:
- **Total Recipients**: Number of individuals the update was sent to.

### Delivery Metrics
The platform provides three main metrics related to the delivery status of the update:
- **Delivered**: Percentage and number of recipients who successfully received the update.
- **Bounced**: Percentage and number of updates that couldn't be delivered.
- **Cleaned**: Percentage and number of updates that were cleaned (typically indicating they were removed due to invalid or redundant data).

### Response Metrics
This section gives insights into how recipients engaged with the update:
- **Responded**: Percentage and number of recipients who replied or interacted with the update.
- **Didn't Respond**: Number of recipients who didn't reply or interact with the update.

There are visual cues such as icons to represent users who responded or didn't.

### Click Through Metrics
Details related to interactions with any embedded links or calls to action within the update:
- **Clicked**: Percentage of recipients who clicked on a link within the update.
- **Opted Out**: Percentage of recipients who chose to opt-out or unsubscribe from receiving future updates.

### Message Type Breakdown
You can see the breakdown of the update based on the method of dispatch:
- **Delivered as SMS**: Number of updates sent as text messages.
- **By Message Type**: Further categorization, such as updates sent domestically (within the United States) or internationally.

### Interactive Visualization
The platform provides graphical representations, such as pie charts, to help visually interpret the data. Hovering over or clicking on these visualizations might provide additional details.