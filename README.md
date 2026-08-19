# Medication Formatter

A simple Bootstrap-based medication formatting tool designed to convert copied medication lists into clean, editable medication instructions that can be individually copied to the clipboard.

## Features

### Medication Parsing
- Paste raw medication data directly into the input box.
- Supports medication lists exported from GP and clinical systems.
- Automatically removes:
  - HTML tags
  - Dates (e.g. `27-Jul-2026`)
  - `LATEST`
  - `FIRST`
  - Pagination text
  - Miscellaneous navigation symbols
  - Item counts

### Formatted Output
Converts raw data such as:

```text
Quetiapine 100mg tablets
one at night (28 tablet)
LATEST
FIRST
```

into:

```text
Quetiapine 100mg tablets one at night
```

Each medication is displayed on its own line.

### Copy Tracking
Each medication line contains a **Copy** button.

When clicked:

- The medication instruction is copied to the clipboard.
- A green ✅ tick appears beside the medication.
- The tick remains visible until the medication is edited.

### Inline Editing
Medication lines can be edited by clicking directly on the text.

When editing:

- The medication text becomes a multi-line text area.
- The text area automatically expands vertically as more text is entered.
- The green tick is removed.
- The Copy button is hidden.
- A Confirm button is displayed.

When Confirm is clicked:

- Changes are saved.
- The text returns to normal view.
- The Copy button reappears.

### Delete Function
Each medication row contains a Delete button positioned on the far left of the row.

Clicking Delete removes the medication from the output list.

### Safety Confirmation Screen
The application starts with a safety confirmation page.

Users must acknowledge:

> "I confirm that I will not input any confidential data into this website"

before accessing the formatter.

This helps reduce accidental entry of confidential or patient-identifiable information.

## Workflow

### Step 1
Paste medication data:

```text
Quetiapine 100mg tablets
one at night (28 tablet)

Lamotrigine 100mg tablets
Twice A Day (56 tablet)
```

### Step 2
Click:

```text
Format Medications
```

### Step 3
Review formatted output:

```text
Delete | Quetiapine 100mg tablets one at night | Copy

Delete | Lamotrigine 100mg tablets Twice A Day | Copy
```

### Step 4
Optionally:
- Edit text
- Confirm changes
- Copy medication
- Delete medication

## Technologies Used

- HTML5
- CSS3
- JavaScript (Vanilla)
- Bootstrap 5

## Intended Use

This tool was created to simplify the formatting of medication information for clinical workflows where medication directions need to be reviewed, amended, and copied individually.

## Confidentiality Notice

This application is intended for use with non-confidential information only.

Do not enter:
- Patient names
- NHS numbers
- Addresses
- Dates of birth
- Any other identifiable personal information

The user remains responsible for ensuring that all data entered complies with local information governance requirements and organisational policies.

## Licence

MIT License
