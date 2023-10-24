# Filters

## Overview:

The filter panel can be found in the /message or /contacts pages.

## AND/OR Functionality:

- **'AND FILTER' Button**: Used to add another filter to the criteria list. Useful for combining queries with the current filter, such as "Has Assigned No AND [another filter]".

- **'OR FILTER' Button**: Allows the user to specify an alternative filter. This broadens the search query.

- **Discard Button**: Used to clear the current filter criteria.

- **Save Segment Button**: After setting the desired criteria, users can save this filter segment for quick access in the future.

## 1. Age Filter

### Overview:
The "Age" filter facilitates segmenting and viewing contacts based on their age. 

#### Fields & Controls:

- **Dropdown Menu**: Allows users to select the criterion for age filtering. Options may include:
  - "Is"
  - "Is not"
  - "Is greater than"
  - "Is less than"
  - Etc.

- **Input Box**: A field where users can enter a specific age. This can be used in conjunction with the dropdown menu to create specific queries, such as "Age is greater than 25".

- **'AND FILTER' Button**: Used to add another criterion within the "Age" filter. Useful for creating more complex queries like "Age is greater than 25 AND less than 50".

- **'OR FILTER' Button**: Allows the user to specify an alternative age criterion. Useful for creating broader queries like "Age is less than 20 OR greater than 50".

- **Discard Button**: Used to clear the current filter criteria.

- **Save Segment Button**: After specifying the desired criteria, users can save this filter segment for quick access in the future.

### Notes:
- Ensure that the age entered is a valid number.
- Provide feedback if the entered age or combination doesn't match any contacts.
- Allow users to combine multiple criteria for refined search results.

---
## 2. Archived Contact Filter

### Overview:
The "Archived Contact" filter enables users to segment and view contacts that have been previously archived in the system.

### Notes:
- Archived contacts are those that have been temporarily removed from the active list but not permanently deleted.
- Useful for users who want to clean up their active contact list without losing the contact information.

---
## 3. Has Assigned Number Filter

### Overview:
The "Has Assigned Number" filter enables users to segment and view contacts based on whether they have been assigned a specific phone number from a list the user has access to.

#### Fields & Controls:

- **Dropdown Menu**: Allows users to select the criterion for filtering based on assigned phone number status. Options include:
  - "Has Assigned No"
  - "Assigned No Is"
  - "Assigned No Isn't"

- **Input Box** (when applicable): A field where users can enter a specific phone number or choose from a dropdown list of available numbers. Used in conjunction with the "Assigned No Is" option.

### Notes:
- Ensure valid phone number format when entering or selecting from the list.
- Provide feedback if the entered or selected phone number doesn't match any contacts or isn't within the user's accessible list.
- When "Assigned No Is" is selected, prompt or display a dropdown for the user to select or input a specific number.
