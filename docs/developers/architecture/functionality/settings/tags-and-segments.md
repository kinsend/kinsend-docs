# Tags & Segments

The **Tags & Segments** feature in Kinsend allows users to categorize and manage their contacts effectively. Tags are a great way to target specific contacts within in an [automation](/developers/architecture/functionality/automations.html) or [update](/developers/architecture/functionality/updates.html) campaign.

## Overview

On the main "Tags & Segments" page, you'll see:

- A section title "Tags & Segments" with a "SETTINGS" label beneath.
- An overview count of tags and segments currently available.
- Options for user interaction, which include "NEW", "RENAME", and "DELETE".

Below this, there's a grid listing:

- Tag names.
- Creation time.
- Number of contacts associated with each tag.

## User Interaction Logic

When **one tag** is selected:

- Users have the option to "NEW" (add a new tag).
- "RENAME" (edit the selected tag).
- "DELETE" (remove the selected tag).

When **multiple tags** are selected:

- Users can "NEW" (add a new tag).
- "DELETE" (remove all the selected tags).

## Add Tag Modal

When adding a new tag:

- The "Add tag" modal will appear.
- Users are prompted to "Choose a name for the new tag".
- There's an input field for naming the tag.
- Buttons "CANCEL" and "SAVE" allow for exiting without saving or saving the new tag respectively.

## Figma Design Reference

For a detailed and interactive view of the "Tags & Segments" design, refer to the Figma project:

[View Tags & Segments Design on Figma](https://www.figma.com/file/RoClPWX4pBbYGwsH2spccj/KinSend?type=design&node-id=409-2541&mode=design&t=kwnOVpxqXz4g2tdY-0)

This link will take you directly to the specific design section for "Tags & Segments".

---

This system ensures that users can effectively manage their tags, segmenting their contacts for better organization and outreach.