# LinkedIn Interactors Parser

A simple web app to parse and organize LinkedIn post interactors data.

## Features

- **Parse LinkedIn Data**: Copy and paste raw LinkedIn interactors text
- **Extract Profile URLs**: Automatically detects and extracts LinkedIn profile URLs
- **Organized Display**: View data in a clean table format with reactions, names, headlines, and profile URLs
- **Clickable Links**: Profile URLs are clickable and open in a new tab
- **Export Options**:
  - Export to CSV file (includes URLs)
  - Copy to clipboard (tab-separated for easy pasting into Excel/Sheets)
- **Beautiful UI**: Modern, responsive design

## How to Use

1. Open `index.html` in any web browser
2. Copy the interactors list from a LinkedIn post
3. Paste the raw text into the textarea
4. Click "Parse Data"
5. View your organized results in the table
6. Export to CSV or copy to clipboard as needed

## Data Format

The app expects LinkedIn interactor data in this format:

```
[reaction_type]
[Name]
View [Name]'s profile [connection info]
· [degree]
[Headline]
```

Example:
```
like
John Doe
View John Doe's profile 1st degree connection
· 1st
Software Engineer at Tech Company
```

## No Installation Required

This is a single HTML file - no dependencies, no build process, no server needed. Just open and use!
