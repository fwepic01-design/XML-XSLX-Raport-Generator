# Release Notes

## Version 1.0.1 (2025-10-17)

### Bug Fixes

#### Fixed Duplicate "Report Generated" Text Issue
- **Issue**: The "Report Generated" text was appearing twice in the output document:
  1. First occurrence: "Report Generated: CreationDate" (from template placeholder)
  2. Second occurrence: "Report Generated: XX.XX.XXXX" (actual date)
- **Root Cause**: Both the [ReplacePlaceholdersWithTemplate] and [ReplacePlaceholders] methods were adding the "Report Generated" text
- **Fix**: Modified the [ReplacePlaceholders] method to remove the duplicate "Report Generated" text addition, since it's already handled in [ReplacePlaceholdersWithTemplate]
- **Result**: "Report Generated" now appears only once in the output document with the correct date format (DD.MM.YYYY)

### Technical Details

The fix ensures that:
1. When using a proper template with "Report Generated: CreationDate" placeholder, it gets replaced with the current date
2. When falling back to the simplified replacement method, it doesn't add a duplicate "Report Generated" text
3. The date format remains consistent as DD.MM.YYYY

### Testing

The fix has been tested with:
- Templates containing the "Report Generated: CreationDate" placeholder
- Templates without the proper structure (fallback scenario)
- Both XML and Excel data sources
- Various project data configurations

The output now correctly displays "Report Generated: XX.XX.XXXX" only once at the beginning of the document.