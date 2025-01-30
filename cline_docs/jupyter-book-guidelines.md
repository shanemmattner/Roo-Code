# Jupyter Book Documentation Guidelines

This document outlines the standards and best practices for maintaining the Roo Code documentation in Jupyter Book format.

## Navigation Structure

### Table of Contents (_toc.yml)
The _toc.yml file is the single source of truth for navigation. It defines:
- Page hierarchy
- Section organization
- Navigation relationships
- Document structure

### Navigation Rules
1. Always use nested sections for related content
2. Keep hierarchy depth reasonable (max 3 levels)
3. Group related pages under common parents
4. Use descriptive section captions

### Example Structure
```yaml
format: jb-book
root: intro
parts:
  - caption: Section Name
    chapters:
    - file: main-topic
      sections:
      - file: subtopic-1
      - file: subtopic-2
```

## File Structure

### Required Elements
1. Every markdown file must include:
   - A title (h1 heading with #)
   - A brief introduction
   - Clear section headings
   - Links to related pages

2. Navigation Links
   - Use relative links (e.g., `[Custom Modes](custom-modes.md)`)
   - Reference pages defined in _toc.yml
   - Maintain bidirectional links between related content

### File Naming
- Use kebab-case for filenames (e.g., `custom-modes.md`)
- Keep names short but descriptive
- Avoid special characters

## Content Structure

### Headers
- Use h1 (#) for page title
- Use h2 (##) for main sections
- Use h3 (###) for subsections
- Maintain logical heading hierarchy

### Cross-References
- Always use relative links with .md extension
- Example: `[Custom Modes](custom-modes.md)`
- Check links work in navigation
- Include links to related content

### Code Blocks
- Use triple backticks with language
- Include descriptive examples
- Show expected output where relevant

## Maintaining Navigation

### Adding New Pages
1. Create the markdown file
2. Add entry to _toc.yml in appropriate section
3. Add cross-references in related pages
4. Rebuild book to verify navigation

### Updating Existing Pages
1. Check current _toc.yml structure
2. Update cross-references if needed
3. Verify navigation hierarchy
4. Rebuild and test navigation

### Rebuilding the Book
```bash
cd submodules/jupyter-book-assistant
source venv/bin/activate
./generate_book.sh
```

## Quality Checklist

### Before Publishing
1. Navigation
   - [ ] Page appears in _toc.yml
   - [ ] Correct hierarchy level
   - [ ] Proper section grouping
   - [ ] Navigation links work

2. Content
   - [ ] Consistent formatting
   - [ ] Complete examples
   - [ ] Clear explanations
   - [ ] Updated cross-references

3. Structure
   - [ ] Proper headings
   - [ ] Logical organization
   - [ ] Related content linked
   - [ ] Navigation paths clear

## Common Issues

### Navigation Problems
- Missing entries in _toc.yml
- Incorrect nesting levels
- Broken cross-references
- Sidebar disappearing

### Content Issues
- Inconsistent formatting
- Missing cross-references
- Incomplete examples
- Unclear progression

## Best Practices

### Documentation Updates
1. Check existing structure in _toc.yml
2. Follow established patterns
3. Update related pages
4. Test navigation thoroughly

### Content Creation
1. Start with outline
2. Include all required elements
3. Add clear examples
4. Cross-reference related content

## Maintenance

### Regular Tasks
- Review navigation paths
- Update cross-references
- Check for broken links
- Verify sidebar behavior

### Updates Process
1. Make content changes
2. Update _toc.yml if needed
3. Update cross-references
4. Build and verify
5. Test navigation in browser

## Troubleshooting

### Navigation Issues
1. Verify page is in _toc.yml
2. Check nesting level
3. Rebuild book
4. Clear browser cache

### Build Problems
1. Check file paths
2. Verify yaml syntax
3. Check for missing files
4. Review build logs

### Link Issues
1. Use .md extension
2. Check file paths
3. Verify _toc.yml entries
4. Test in built site