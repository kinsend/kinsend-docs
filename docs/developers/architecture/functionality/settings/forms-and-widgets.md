# Forms & Widgets

- [Forms test cases](https://github.com/kinsend/kinsend-be/issues/175)
- [CNAMEs test cases](https://github.com/kinsend/kinsend-be/issues/165)
- [Forms submissions test cases](https://github.com/kinsend/kinsend-be/issues/168)
- [Custom fields test cases](https://github.com/kinsend/kinsend-be/issues/183)

## **Overview**
The "Forms" feature in KinSend offers users the capability to create opt-in landing pages. These are designed to capture lead information, which can be pivotal for text message marketing campaigns in the future.

## **Key Features**

1. **Customization**: Forms can be tailored to inquire virtually any information from a potential lead.
2. **Multiple Forms Creation**: Users have the flexibility to construct as many diverse forms as they need.
3. **Custom Domain Name**: Users can select a custom CNAME for their Forms under the domain name `app.kinsend.io`.

## **Detailed Features**

- **KinSend URL**: This represents the public URL to your address book form. Users can select a custom CNAME for their Forms under the domain name `app.kinsend.io`.
- **Inbound Tag**: Designate specific tags to be applied to incoming contacts. It's an efficient way to segment specific subscribers to an automation.
- **Title & Browser Title**: Define the public facing title of your form and how it should appear in the browser's tab respectively.
- **Custom Redirect URL**: Post submission, new subscribers will be redirected to this URL. If left blank, they'll be navigated to a default submission success page.
- **Description**: Explain your intention behind the form, allowing subscribers to understand the information they provide and the benefits they receive.
- **Optional Fields**: Fields that aren't mandatory but can provide additional information about the lead. Optional fields can include:
    - Gender
    - Birthday
    - Twitter Handle
    - Instagram Handle
    - LinkedIn Handle
    - Job
    - Title
    - Company
    - Industry
- [**Custom Fields**](#custom-fields): These allow the capturing of diverse information. Users can decide which questions they want to incorporate into their public form.
- **Form Submission**: Configure settings such as the message to be sent via SMS upon form completion.
    - The "Enabled" checkbox must be checked in order for this message to be sent upon a subscriber's completion of the form. If it is unchecked then the message will still be saved within the form settings but just not sent to subscribers upon form completion.
    - The vCard checkbox, if checked, will send the subscriber your vCard upon completion of form. The vCard checkbox can only be selected if a user has configured their vCard already.
- **Form Submission Success Page Message**: Customize the message seen by users once they've successfully submitted the form.

## **Custom Fields**

Custom fields offer the flexibility for users to curate specific questions tailored to their needs, especially ones that resonate with their industry. These questions can play a crucial role in capturing more nuanced information from contacts.

The KinSend platform provides the following types of custom fields:

- **Single Line Text**: For short, concise responses, such as names or unique identifiers. 
  - **Inbound Tag**: Specify which tag(s) should be applied to incoming contacts. This helps in categorizing or segmenting contacts based on their responses.
  - **Label Question**: Define the question or statement that prompts the user for input.
  - **Placeholder Text**: Provide a hint or example to guide users on what to type in.
  - **Required**: Toggle this option if you want to make this field mandatory for the user to fill out.
  
  To create a Single Line Text field:
  1. Choose "Single Line Text" from the "SELECT TYPE" dropdown in the "Custom Fields" modal.
  2. Configure the aforementioned options as per your requirements.
  3. Click `SAVE` to finalize and add the custom field.

- **Paragraph Text**: Suitable for longer responses, like feedback or detailed explanations.
  - **Inbound Tag**: Specify which tag(s) should be applied to incoming contacts. This helps in categorizing or segmenting contacts based on their responses.
  - **Label Question**: Define the question or statement that prompts the user for input.
  - **Placeholder Text**: Provide a hint or example to guide users on what to type in.
  - **Required**: Toggle this option if you want to make this field mandatory for the user to fill out.
  
  To create a Paragraph Text field:
  1. Choose "Paragraph Text" from the "SELECT TYPE" dropdown in the "Custom Fields" modal.
  2. Configure the aforementioned options as per your requirements.
  3. Click `SAVE` to finalize and add the custom field.

- **Single Choice (Radio)**: Allows subscribers to pick only one option from a set of choices.
  - **Label Question**: Define the question or statement that prompts the user for a choice.
  - **Options**: List the choices available for users to select. Each option can also have an associated tag to help categorize or segment contacts based on their selection.
  - **Required**: Toggle this option if you want to make this field mandatory for the user to select an option.
  
  To create a Single Choice (Radio) field:
  1. Choose "Single Choice (Radio)" from the "SELECT TYPE" dropdown in the "Custom Fields" modal.
  2. Configure the aforementioned options as per your requirements.
  3. Click `SAVE` to finalize and add the custom field.

- **Single Choice (Select)**: Presents a dropdown menu for users to select one choice from multiple options.
  - **Label Question**: Define the question or statement that prompts the user for a choice.
  - **Options**: List the choices available for users to select. Each option can also have an associated tag to help categorize or segment contacts based on their selection.
  - **Required**: Toggle this option if you want to make this field mandatory for the user to select an option.
  
  To create a Single Choice (Select) field:
  1. Choose "Single Choice (Select)" from the "SELECT TYPE" dropdown in the "Custom Fields" modal.
  2. Configure the aforementioned options as per your requirements.
  3. Click `SAVE` to finalize and add the custom field.

- **Checkboxes**: Lets subscribers select multiple options from a list. Suitable for questions where multiple answers are acceptable.
  - **Label Question**: Define the question or statement that prompts the user for their choices.
  - **Options**: List the choices available for users to select. Each option can have an associated tag to help categorize or segment contacts based on their selection.
  - **Required**: Toggle this option if you want to make this field mandatory for the user to select at least one option.
  
  To create a Checkboxes field:
  1. Choose "Checkboxes" from the "SELECT TYPE" dropdown in the "Custom Fields" modal.
  2. Configure the aforementioned options as per your requirements.
  3. Click `SAVE` to finalize and add the custom field.

To create a custom field:

1. Navigate to the "Custom Fields" modal in /settings/forms and hit the "Custom Fields" tab.
2. Click the `+ NEW` button.
3. From the "SELECT TYPE" dropdown, choose the desired custom field type.
4. Define your custom question and save it.

