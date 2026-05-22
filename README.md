# WordUtil

WordUtil is a reusable Mendix Marketplace module that provides Microsoft Word document utilities using Java Actions.

The module currently supports:

- Find and replace text in Word documents
- Merge multiple Word documents into a single document

## Features

### JA_FindAndReplace

Finds placeholders or text inside a Word document and replaces them dynamically.

#### Use Cases

- Generate offer letters
- Generate invoices
- Generate reports
- Template-based document generation

### JA_MergeDocuments

Merges multiple Word documents into a single document.

#### Use Cases

- Merge generated reports
- Combine chapter documents
- Export consolidated documents

---

# Supported Mendix Versions
- Mendix 10.24.16

---

# Dependencies

The module uses Apache POI libraries for Word document processing.

# Installation

1. Download the module from Mendix Marketplace.
2. Import the module into your Mendix project.
3. Ensure required Apache POI dependencies exist in `userlib`.
4. Use the Java actions in microflows.

---

# Java Actions

## 1. JA_FindAndReplace

### Description

Replaces text placeholders inside a `.docx` file.

### Parameters

| Parameter      | Type         | Description          |
| -------------- | ------------ | -------------------- |
| InputDocument  | FileDocument | Source Word document |
| SearchText     | String       | Text to find         |
| ReplaceText    | String       | Replacement text     |
| OutputDocument | FileDocument | Generated document   |

### Example

Find:

```text
${EmployeeName}
```

Replace with:

```text
Amit Gupta
```

---

## 2. JA_MergeDocuments

### Description

Merges multiple `.docx` files into one document.

### Parameters

| Parameter      | Type                 | Description           |
| -------------- | -------------------- | --------------------- |
| DocumentList   | List of FileDocument | Documents to merge    |
| OutputDocument | FileDocument         | Final merged document |

---

# Example Microflow Usage

```text
1. Upload Word template
2. Call JA_FindAndReplace
3. Generate personalized document
4. Merge documents using JA_MergeDocuments
5. Provide final downloadable file
```

---

# Best Practices

* Use `.docx` format only
* Keep placeholder naming consistent
* Validate uploaded files before processing
* Avoid extremely large document merges

---


# Future Enhancements

Planned improvements:

* Table placeholder replacement
* Header/Footer replacement
* PDF conversion support
* Image replacement
* Mail merge functionality

---

# Contributing

Contributions are welcome.

You can:

* Raise issues
* Suggest enhancements
* Submit pull requests

---


# Author

Amit Gupta

Mendix Developer

---
