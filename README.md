# Google Docs Markdown Converter

## Brief Description

This tool converts Markdown content to Google Docs format with proper styling and formatting.

### Key Features:
- Smart Markdown Parsing: Automatically detects headings (H1, H2, H3), bullet points, checkboxes, and separators
- Rich Formatting: Converts Markdown to properly styled Google Docs with headings, lists, and text formatting
- Assignee Highlighting: Automatically highlights @mentions in bold with custom colors
- Footer Styling: Automatically formats footer content with italic styling
- Nested Lists: Supports indented bullet points and checkboxes for complex hierarchies

## Setup Instructions

### Prerequisites
- Google account with access to Google Docs
- Python 3.6 or higher

### Quick Start

Upload the `md_to_google_doc.ipynb` notebook to Google Colab and open it.

## Required Dependencies

The notebook automatically installs the following dependencies:

- `google-api-python-client` - Google API client library
- `google-auth-httplib2` - Google authentication library  
- `google-auth-oauthlib` - Google OAuth 2.0 library

These are installed automatically when you run the first cell in the notebook.

## How to Run in Colab

Execute the notebook cells in order:
1. Install Required Dependencies
2. Authenticate with Google  
3. Define Markdown parsing functions
4. Define main converter class
5. Run the example conversion

### Expected Output

When successful, you'll see:
```
Installing Required Dependencies...
Authenticating with Google Docs API...
Google Docs API authenticated
Creating Google Doc...Created document: Product Team Sync - Meeting Notes
Conversion completed

Document is ready @: https://docs.google.com/document/d/[DOCUMENT_ID]/edit
```

### Quick Usage Example

```python
# Create converter instance
converter = GoogleDocConverter()

# Create document
converter.create_document("My Meeting Notes")

# Convert markdown content
markdown_content = """
# Meeting Title

## Agenda
- Discuss project progress
- Plan next steps

## Action Items
- [ ] @john: Complete the report
"""

converter.convert(markdown_content)
```

---

**Note**: This tool requires internet access and Google authentication to function properly. Your Markdown content is processed locally and only the formatted result is sent to Google Docs.
