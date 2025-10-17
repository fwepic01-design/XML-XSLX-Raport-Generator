# Release Notes

## v1.0.2 - Multi-language Support with Menu Bar ( in progress)
*Added: Multi-language support for the user interface*
- Added language selection through menu bar (English, Polish, Spanish)
- All UI elements now translate based on selected language
- Error messages and status texts are now localized
- Default language is Polish (maintaining backward compatibility)
- Language menu is positioned at the top of the application for easy access
- Fixed menu bar visibility issues

## v1.0.1 - Duplicate Text Fix
*Fixed: Duplicate "Report Generated" text issue*
- Resolved issue where "Report Generated" text appeared twice in output documents
- Removed duplicate addition in the fallback template processing method
- Maintained proper functionality for both template-based and fallback processing

## v1.0.0 - Initial Release
*Initial release of the Excel to Word Converter*
- Load data from Excel files (.xlsx, .xls) or XML files
- Use customizable Word templates for report generation
- Process project data with project numbers and dates
- Groups data by project number
- Calculates date ranges and sums hours
- Generates Word documents with auto-generated filenames

