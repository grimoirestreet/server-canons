# Staff Instructions: Adding New Canon Entries

## Quick Start
1. Navigate to the `lore-data.json` file in your GitHub repository
2. Click the pencil icon (✏️) to edit
3. Add your new entry following the format below
4. Commit your changes

## Adding a New Canon Entry

Find the end of the file (after the last `}` but before the closing `]`) and add a comma, then your new entry:

```json
  ,
  {
    "type": "Rules",
    "location": "Your Canon Title Here",
    "creator": "SERVER LORE",
    "lore": "The main description of your canon rule or lore. This should be detailed and clear.",
    "notes": "Optional additional notes, OOC information, or clarifications."
  }
```

## Field Explanations

- **type**: Must be one of: `"Rules"`, `"Magic"`, `"Location"`, `"General"`
- **location**: The title/name of this canon entry (what players will see as the heading)
- **creator**: Usually `"SERVER LORE"`, `"CANON"`, or `"CANON / SERVER LORE"`
- **lore**: The main description - this is the core information
- **notes**: Optional field for additional context, OOC notes, etc. Can be left empty with `""`

## Example Entry

```json
  ,
  {
    "type": "Rules",
    "location": "Owl Post Regulations",
    "creator": "SERVER LORE",
    "lore": "All student mail must be sent through school owls during term time. Personal owls may only be used for emergency family communications with prior approval from a Head of House.",
    "notes": "OOC note: Players should still feel free to have their characters receive letters for plot purposes - this rule exists for world-building consistency."
  }
```

## Important Notes

- **Always add a comma** after the previous entry before adding your new one
- **Don't add a comma** after your new entry if it's the last one
- **Check your JSON formatting** - missing quotes or brackets will break the site
- **Test the site** after making changes to ensure it loads properly
- **Use straight quotes** (`"`) not curly quotes (`"`)

## Types Available

- **Rules**: School rules, regulations, laws
- **Magic**: Spells, magical items, magical concepts  
- **Location**: Places, buildings, areas
- **General**: Everything else (events, people, atmosphere, etc.)

## Editing Existing Entries

1. Find the entry you want to modify in the `lore-data.json` file
2. Click the pencil icon to edit
3. Make your changes to the `"lore"` or `"notes"` fields
4. Commit your changes

## Troubleshooting

If the site breaks after your changes:
1. Check for missing commas between entries
2. Ensure all quotes are properly closed
3. Verify brackets `{}` are properly matched
4. Look for any special characters that might need escaping

The site will automatically update within a few minutes of committing your changes to GitHub!
