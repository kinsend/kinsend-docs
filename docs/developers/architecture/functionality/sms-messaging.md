# SMS messaging
## 1.1 Overview
- **1 to 1 SMS messaging**: Occurs on the `/message` page.
- **User's message threads**: All encompassed on this page.
- **Chronological order**: Latest messages displayed at the top by default.
- **Sorting Options**: Contacts can be sorted by:
    - Chronological order
    - Messages exchanged (both outbound and inbound)
    - Inbound messages
    - Outbound messages
- **Unread messages**: Displayed with a counter indicating the number of unread messages.
- **Message Filtering**: Messages can be filtered by Age, Archived Contact, Archived Conversation, Assigned Number, Automated Conversation, Birthday, Company, Contact, Created Date, Email, Facebook Contact, Form Completed, Gender, Hidden Conversation, Industry, Job Title, Last Contacted, Last Updated, Link Clicked Update, Lives In, Messages Exchanged, Messages Incoming, Messages Outgoing, Mobile, Opted-Out, Replied, Responded to Update, Sent Update, Subscribed, Tagged, Unknown Number, Unread Conversation, VIP. For more details on filters, see [filters](/developers/architecture/functionality/filters.html).

## 1.2 Conversations List Panel
### Display
- **[Dialer Icon](#2-voice-call-modal)**: Opens the Dialer Modal
- **[Pencil Icon](#3-message-contacts-modal)**: Opens the Message Contacts Modal
- **Recent Conversations**: List showcasing contact's initials or image, name, latest message snippet, and timestamp.
- **Search Bar**: Facilitates specific conversation searches.

### Functionality
- **Active Conversation**: Clicking on an item loads it into 'Conversation Detail Panel'.
- **Right-click Options**: Delete/archive conversations and mark them as unread.

## 1.3 Conversation Detail Panel
### Display
- **Contact Details**: Name at the top with a profile view option.
- **Messages**: Continuous scroll with timestamps, alignment and color codes differentiate message types.
- **Media Attachments**: Images, videos, and documents within the conversation.

### Functionality
- **Sending Options**: Users can dispatch text messages, media, and links.
- **Media Handling**: Download or view in full-screen.
- **Message Options**: Right-click to delete, copy, forward, or flag.
- **Status Display**: Showcases message statuses such as Sent, Delivered, Read.
- **vCard**: Download option if available.

## 1.4 Contact Information Panel
### Display
- **Profile Data**: Contact's name, image, and tags (e.g., "Kinsend Lead").
- **Contact Info**: Email, Messaging ID, Mobile, and Assigned number.
- **Interaction History**: Last contact time and transactional data.

### Functionality
- **Direct Options**: Call or message the contact.
- **Editing**: Update contact details.
- **Assignment & Tagging**: Delegate contact to another or add tags.

---
## 2. Voice Call Modal
### 2.1 Header
- **Title**: "Voice Call".
- **Description**: "Search for the contact you want to call or use the dial pad to dial a number."

### 2.2 Contact Search and Dial Field
- **Input Box**: Allows users to either search for a contact by name or directly enter a phone number.
- **Placeholder**: "Find a contact or enter a number".
- **Dropdown**: Provides suggestions for contacts based on input.

### 2.3 Dial Pad and Call Options
- **Dial Pad Icon**: Opens up a numerical dial pad for manual number entry.
- **Call Button**: Initiates the voice call.
- **Emoji/Emoticon Button**: Allows users to send emojis or emoticons.

### 2.4 Exit Option
- **Close Icon**: Positioned at the top-right corner to exit the modal.

---
## 3. Message Contacts Modal
### 3.1 Header
- **Title**: "Message Contacts".
- **Guide**: "Start a conversation with one or several contacts. To broadcast a message to all of your contacts or a chosen segment, Check Out Updates."

### 3.2 Recipient Field
- **Contact Display**: Name and phone number shown.
- **Deselect Icon**: 'x' option to remove a chosen contact.

### 3.3 Message Input Box
- **Placeholder**: "Enter text..."
- **Character Counter**: E.g., "160".

### 3.4 Emoji & Attachment Icons
- **Emoji Picker**: Facilitates emoticon selection.
- **File Picker**: Attach files to the message.

### 3.5 Scheduled Toggle
- **Label**: "Scheduled".
- **Description**: "SuperPhone will send your message at a future scheduled date."

### 3.6 Send Button
- **Label**: "SEND".
- **Disabled State**: If no text or recipients are chosen.
