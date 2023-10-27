# Tags & Segments

[Tags test cases](https://github.com/kinsend/kinsend-be/issues/184)
[Segments test cases](https://github.com/kinsend/kinsend-be/issues/178)

The **Tags & Segments** feature in Kinsend allows users to categorize and manage their contacts effectively. Tags are a pivotal tool for targeting specific contacts within an [automation](/developers/architecture/functionality/automations.html) or [update](/developers/architecture/functionality/updates.html) campaign.

## Overview

On the main "Tags & Segments" page, you'll observe:

- A section title `Tags & Segments` with a `SETTINGS` label beneath.
- An indicator displaying the total number of tags, providing a quick overview of the tags created in the system.
- User interaction options: `NEW`, `RENAME`, and `DELETE`.
- A grid showcasing:
  * Tag names
  * Creation time
  * Number of contacts associated with each tag

## User Interaction Logic

- **Single Tag Selection**:
  * Options to `NEW` (add a new tag).
  * `RENAME` (edit the selected tag).
  * `DELETE` (remove the selected tag).

- **Multiple Tags Selection**:
  * Option to `NEW` (add a new tag).
  * `DELETE` (remove all the selected tags).

## Add Tag Modal

When adding a new tag:

- A `Add tag` modal appears.
- Users are prompted to "Choose a name for the new tag".
- An input field for naming the tag is present.
- `CANCEL` and `SAVE` buttons for either exiting without saving or saving the new tag.

## Pagination in Tags & Segments

To streamline tag management, the "Tags & Segments" page offers a pagination system.

### Features

- **Page Numbers**: At the grid's bottom, users encounter a sequence of numbers. Each represents a tag page.
- **Navigation Arrows**: Adjacent to the page numbers are navigation arrows (`<` and `>`). The left arrow navigates to the previous page, and the right one leads to the subsequent page.

### Usage

This pagination system bolsters the efficient management and organization of multiple tags. For quicker access to tags towards a list's end, users can employ the navigation arrows or directly select higher page numbers.

## Figma Design Reference

For a detailed "Tags & Segments" design view, refer to the Figma project:

[View Tags & Segments Design on Figma](https://www.figma.com/file/RoClPWX4pBbYGwsH2spccj/KinSend?type=design&node-id=409-2541&mode=design&t=kwnOVpxqXz4g2tdY-0)

Clicking the link takes you straight to the specific "Tags & Segments" design section.
