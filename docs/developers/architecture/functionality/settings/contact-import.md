# Contact Import

[Contacts test cases](https://github.com/kinsend/kinsend-be/issues/185)

## Overview
The "Contact Import" feature allows users to import contacts from a CSV or XLSX file into the system. This feature ensures easy migration or addition of contacts without the need for manual entry.

## User Interface

### Screenshot 1:
![Initial Import Page](/assets/images/contact-import-screenshot1.png)
*Description:* This screenshot displays the primary interface for the contact import feature. Users can upload a CSV or XLSX file. There's an important note ensuring that the table includes columns for the First Name and either Phone Number or Email.

## Data Fields

The following are the fields that the CSV or XLSX file can contain. Note: "Phone Number" and "First Name" are mandatory fields.

- **First Name** *(Required)*
- **Phone Number** *(Required)*
- Last Name
- Email
- Job Title
- Company
- Address1
- Address2
- City
- State/Province
- Country Code
- Zip Code
- Tags
- Gender
- Birthday
- Instagram
- Twitter

## Guidelines for Import

1. Ensure the CSV or XLSX file adheres to the required format.
2. Mandatory fields (First Name and Phone Number) must be present in the file; otherwise, the upload will fail.
3. Additional fields can enhance the contact's information but are optional.
4. Once uploaded, users can verify and manage the imported contacts within the platform.

### Screenshot 2:
![Mapping Fields](/assets/images/contact-import-screenshot2.png)
*Description:* This screenshot provides a view of the mapping interface. After uploading a CSV or XLSX file, users can map the columns in their file to the respective fields in Kinsend. This ensures that the imported data is correctly aligned with Kinsend's system.

## Mapping Process

1. **File Upload:** Users start by uploading their desired CSV or XLSX file.
2. **Column Mapping:** Users can select which data they want to match to their file columns by selecting the appropriate option from the dropdown menus.
    - Example: If a user's file has a column titled "First Name," they can map it to the "First Name" field in Kinsend.
3. **Preview:** A preview shows the mapped data. In the provided example, columns like "First Name," "Last Name," "Phone," "Email," and "Job Title" are displayed with sample data.
4. **Validation:** An alert is displayed if mapping is incorrect, guiding users to ensure their table includes mandatory columns like "First Name" and "Phone Number." For reference, here is how we should be validating each field.
>
STANDARD/CUSTOM | NAME | DATA TYPE | REQUIRED/OPTIONAL |
-- | -- | -- | --
Standard | Email | Email |  Required |
Standard | Phone Number | Phone Number | Required |
Standard | First Name | Plain Text | Optional |
Standard | Last Name | Plain Text | Optional | 
Standard | Tags | Array of Plain Texts | Optional |
Standard | Birthday | Date | Optional |
Standard | Job Title | Plain Text | Optional |
Standard | Notes | Plain Text | Optional |
Standard | Company | Plain Text | Optional |
Standard | Industry | Plain Text | Optional |
Standard | Instagram | Plain Text | Optional |
Standard | Twitter | Plain Text | Optional |
Standard | LinkedIn | Plain Text | Optional |
Standard | Complete Address | Plain Text | Optional | 
Standard | Address 1 | Plain Text | Optional |
Standard | Address 2 | Plain Text | Optional |
Standard | Zip Code | Plain Text | Optional |
Standard | Country Code | Plain Text | Optional |
Standard | State/Province | Plain Text | Optional |
Standard | City | Plain Text | Optional |
Standard | Latitude | Number | Optional |
Standard | Longitude | Number | Optional |
Standard | Gender | Plain Text |Optional

5. **Proceed:** After successfully mapping all desired columns, users can proceed by clicking the "NEXT" button.

### Screenshot 3:
![Final Details](/assets/images/contact-import-screenshot3.png)
*Description:* This screenshot depicts the final steps of the contact import process.

## Final Details

1. **Inbound Tag:** Users can select a tag to be applied to the newly imported contacts. This helps categorize and manage contacts effectively.
2. **Override Pre-existing Contact Information:** A checkbox is provided to let users decide if they want to skip importing contacts that already exist in the system or override their information. ANY FIELD can be overwritten with the exception of Phone Number. That is the field we use to search for existing subscriber entries in the database.
3. **Import Button:** After ensuring all details are correctly set, users can initiate the import process by clicking the "IMPORT" button.


