# LinkedIn Interactors Parser

A simple web app to parse and organize LinkedIn post interactors data.

## Features

- **Excel File Upload**: Upload an Excel file with hyperlinked text to preserve LinkedIn profile URLs
- **Multi-Sheet Support**: Analyze multiple profiles at once - each sheet represents a different person's interactors
- **Network Overlap Analysis**: Visual network analysis showing which profiles share common interactors
- **Profile Filtering**: Filter results by specific profile or view all at once with dropdown selector
- **Duplicate Detection**: Find people who engage with multiple profiles - your biggest fans and influential connectors
- **Keyword Analytics**: Search for job titles, industries, or skills and see visual analytics with counts and percentages
- **Profile Segmentation**: Keep interactors organized by which profile they interacted with
- **Parse LinkedIn Data**: Copy and paste raw LinkedIn interactors text
- **Extract Profile URLs**: Automatically detects and extracts LinkedIn profile URLs from Excel hyperlinks
- **Organized Display**: View data in a clean table format with profile source, reactions, names, headlines, and profile URLs
- **Clickable Links**: Profile URLs are clickable and open in a new tab
- **Export Options**:
  - Export to Excel file with separate sheets for each profile
  - Copy to clipboard (tab-separated, respects current filter)
- **Beautiful UI**: Modern, responsive design with visual analytics

## How to Use

### Option 1: Upload Excel File (Recommended - Preserves Hyperlinks)

**Single Profile:**
1. Open `index.html` in any web browser
2. Copy the interactors from a LinkedIn post into Excel (Column A)
   - Paste into a single column
   - The hyperlinks will be preserved in Excel
3. Save the Excel file (.xlsx or .xls)
4. Click "Choose Excel File" and select your file
5. The app will automatically parse and display the results with URLs intact
6. Export to CSV or copy to clipboard as needed

**Multiple Profiles (Multi-Sheet):**
1. Create an Excel file with multiple sheets
2. Name each sheet after the profile you're analyzing (e.g., "John Doe", "Jane Smith")
3. In each sheet, paste the LinkedIn interactors data in Column A
4. Upload the Excel file
5. The results will show all interactors with a "Profile" column indicating which sheet/person they came from
6. Export keeps all profiles organized in one file with the Profile column

**Example Multi-Sheet Structure:**
```
Sheet 1: "John Doe"
  - Antonio Grasso
  - Illia Khamza
  - ...

Sheet 2: "Jane Smith"
  - Chris Peters
  - Vicki Beech
  - ...
```

Result: Combined table showing all interactors with their source profile clearly labeled.

### Filtering and Analytics

**Filter by Profile:**
- Use the "Filter by Profile" dropdown at the top of results
- Select a specific profile to view only their interactors
- Select "All Profiles" to view everyone together
- The count updates to show filtered results

**Duplicate Detection:**
- Check "Show Duplicates Only" to see people who appear across multiple profiles
- Duplicates show a golden badge with "×N profiles"
- See which profiles each person engaged with
- Perfect for finding your most loyal connections and influential network nodes

**Network Overlap Analysis:**
- Automatically appears when analyzing 2+ profiles
- Shows summary stats: profiles analyzed, profile pairs, unique people, largest overlap
- Visual overlap matrix for each profile pair:
  - Shared connection count with progress bars
  - Overlap percentage (shared / total unique)
  - Lists first 5 shared names (e.g., "John Smith, Jane Doe, Bob Wilson + 12 more")
- Sorted by overlap size (largest first)
- Use cases:
  - Find strongest network connections between people
  - Identify shared audience or community
  - Discover influential connections who engage with multiple profiles
  - Understand network clustering patterns

**Keyword Analytics:**
- Enter keywords separated by commas (e.g., "CEO, Engineer, Marketing, AI")
- Click "Analyze" to generate statistics
- See count and percentage for each keyword with visual bar graphs
- Table automatically filters to show only matching headlines
- Use cases:
  - Analyze audience composition by job title
  - Find industry representation (Finance, Tech, Healthcare)
  - Identify skill concentrations (AI, Design, Sales)
  - Measure engagement from specific roles

**Combined Filters:**
- All filters work together
- Example: "Show me duplicates who are CEOs" (check duplicates + search "CEO")
- Status badge shows all active filters

### Exporting

**Export to Excel:**
- Click "Export to Excel" button
- Each profile is exported to a separate sheet
- Sheet names match the profile names
- All profiles are included regardless of current filter
- File format: .xlsx (Excel)

**Copy to Clipboard:**
- Click "Copy to Clipboard" button
- Copies data in tab-separated format
- Respects current filter (only copies visible data)
- Paste directly into Excel, Google Sheets, or other tools

### Option 2: Paste Text Data

1. Open `index.html` in any web browser
2. Copy the interactors list from a LinkedIn post
3. Paste the raw text into the textarea
4. Click "Parse Data"
5. View your organized results in the table
6. Export to CSV or copy to clipboard as needed

**Note**: When pasting text directly, hyperlinks are lost. Use the Excel upload method to preserve LinkedIn profile URLs.

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
