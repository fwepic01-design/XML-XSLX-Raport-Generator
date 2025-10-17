# Inportant Info

**First**
Source Code Files will be updated every Major version
**Second (How versions work)**
1 - Major Version
.0 - Major Bug Fix
.0 - Not inportant minimall fix
 

# Template-Based Report Generation System

## Overview

This document describes the enhanced template-based report generation system that can process XML data files and generate Word documents using customizable templates with repeating sections for each project.

## Template Structure

The system supports templates with the following structure:

```
Report Generated: CreationDate

Project: ProjectNumber
Date: DateRange
Hours: ProjectHours

---

Summary:

Total Hours: TotalHours
```

## How It Works

1. **Template Identification**:
   - The system scans the template document to identify the project section
   - It looks for paragraphs containing "Project:" to mark the beginning
   - It looks for paragraphs containing "---" to mark the end of the project section
   - It looks for paragraphs containing "Summary:" to identify where to place the total hours

2. **Data Processing**:
   - For each project in the XML/Excel file:
     - The system clones the project template section
     - Replaces placeholders with actual project data:
       - "ProjectNumber" → Actual project number
       - "DateRange" → Formatted date range (e.g., "15.01.2025-16.01.2025" or "15.01.2025" if single date)
       - "ProjectHours" → Total hours for the project
     - Inserts the filled template into the document

3. **Summary Generation**:
   - Calculates total hours across all projects
   - Places the summary in the designated section

## Example

### Input XML:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<projects>
  <project>
    <nr_projektu>PROJ001</nr_projektu>
    <data>2025-01-15</data>
    <godziny>8.5</godziny>
  </project>
  <project>
    <nr_projektu>PROJ001</nr_projektu>
    <data>2025-01-16</data>
    <godziny>7.0</godziny>
  </project>
  <project>
    <nr_projektu>PROJ002</nr_projektu>
    <data>2025-01-20</data>
    <godziny>6.0</godziny>
  </project>
</projects>
```

### Template:
```
Report Generated: CreationDate

Project: ProjectNumber
Date: DateRange
Hours: ProjectHours

---

Summary:

Total Hours: TotalHours
```

### Generated Output:
```
Report Generated: 16.10.2025

Project: PROJ001
Date: 15.01.2025-16.01.2025
Hours: 15.5

Project: PROJ002
Date: 20.01.2025
Hours: 6.0

---

Summary:

Total Hours: 21.5
```

## Key Features

1. **Flexible Template System**:
   - Users can create any .docx template with the required structure
   - Placeholders are clearly defined and easy to use
   - Template sections are automatically identified and processed

2. **Repeating Sections**:
   - Each project gets its own section in the output
   - Sections maintain the formatting from the template
   - Automatic spacing between projects

3. **Automatic Data Processing**:
   - Date range calculation (from-to or single date)
   - Hour summation per project
   - Total hours calculation across all projects

4. **Multiple Data Sources**:
   - Supports both XML and Excel input files
   - Consistent processing regardless of data source

## Implementation Details

The system uses the DocumentFormat.OpenXml library to:
1. Parse the template document
2. Identify and extract template sections
3. Clone and modify sections for each project
4. Insert filled sections into the document
5. Update the summary section with total hours

The template processing algorithm:
1. Scans the document to find template sections
2. Extracts the project template
3. Removes the original template from the document
4. For each project:
   - Clones the template
   - Replaces placeholders with project data
   - Inserts the filled template into the document
5. Adds the summary section with total hours

This approach provides maximum flexibility while maintaining ease of use for end users.
