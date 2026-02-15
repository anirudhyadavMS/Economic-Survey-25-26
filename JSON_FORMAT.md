# Chapter JSON Format Documentation

This document describes the JSON schema used for chapter data files in the Economic Survey 2025-26 application.

## File Naming Convention

Chapter JSON files follow the naming pattern: `chapter_XX.json` where XX is the chapter number (01-17).

## JSON Schema

Each chapter JSON file contains the following structure:

```json
{
  "id": number,           // Chapter ID (1-17)
  "icon": "string",       // Emoji icon for the chapter
  "title": "string",      // Full chapter title (e.g., "Chapter 1: State of the Economy")
  "subtitle": "string",   // Chapter subtitle/tagline
  "pages": "string",      // Page range (e.g., "2-37")
  "summary": "string",    // Executive summary paragraph
  "keyPoints": [          // Array of key points
    "string",
    ...
  ],
  "whyMatters": "string", // Why this chapter matters for career/understanding
  "introduction": "string", // Chapter introduction text
  "sections": [           // Hierarchical content sections
    {
      "type": "major",    // Section type: "major", "collapsible", or "box"
      "icon": "string",   // Section icon
      "title": "string",  // Section title
      "description": "string", // Section description
      "subsections": [    // Array of subsections (recursive structure)
        {
          "type": "collapsible",
          "number": "string",     // Section number (e.g., "1.1")
          "title": "string",      // Subsection title
          "summary": "string",    // Mini summary
          "content": ["string"]   // Array of content paragraphs
        },
        {
          "type": "box",
          "title": "string",      // Box title
          "content": "string"     // Box content (can be HTML)
        }
      ]
    }
  ]
}
```

## Section Types

### 1. Major Section
Represents a main section heading with subsections.

```json
{
  "type": "major",
  "icon": "📑",
  "title": "SECTION TITLE",
  "description": "Section description",
  "subsections": [...]
}
```

### 2. Collapsible Section
Represents an expandable/collapsible content section.

```json
{
  "type": "collapsible",
  "number": "1.1",
  "title": "Subsection Title",
  "summary": "Brief summary of the section",
  "content": [
    "Paragraph 1",
    "Paragraph 2",
    ...
  ]
}
```

### 3. Box Section
Represents a special highlighted box with detailed information.

```json
{
  "type": "box",
  "title": "Box Title",
  "content": "Detailed content (can include HTML)"
}
```

## Usage in Application

The application loads these JSON files dynamically when a user clicks on a chapter:

1. **Fetching**: `loadChapterFromJSON(id)` fetches the JSON file
2. **Rendering**: `renderChapterContent(data)` generates HTML from JSON
3. **Display**: Content is injected into the chapter div

## Example

See `chapter_01.json` for a complete example of the chapter format.

## Benefits

- **Separation of Concerns**: Content separated from presentation
- **Easy Maintenance**: Update content without modifying HTML
- **Data Portability**: JSON can be consumed by other applications
- **Version Control**: Clear diffs when content changes
- **Scalability**: Easy to add new chapters

## Fallback Mechanism

If JSON loading fails (e.g., network error, file not found), the application falls back to hardcoded HTML content in `index.html`, ensuring the application remains functional.

## Validation

All JSON files have been validated for:
- ✅ Proper JSON syntax
- ✅ Required fields present
- ✅ No XSS vulnerabilities
- ✅ Consistent data structure
