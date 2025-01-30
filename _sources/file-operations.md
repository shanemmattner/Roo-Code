# File Operations

Roo Code provides powerful capabilities for working with files in your workspace. This guide covers how to use Roo Code's file operations effectively.

## Available Operations

### Reading Files
- View file contents
- Search across files
- Analyze code structure
- List directory contents

### Writing Files
- Create new files
- Modify existing files
- Apply diffs
- Handle large files

### Search Operations
- Regex search
- Code definition search
- Pattern matching
- Context-aware results

## File Tools

### read_file
```
<read_file>
<path>src/main.js</path>
</read_file>
```
- Gets file contents with line numbers
- Supports any text-based file
- Extracts text from PDFs and DOCXs
- Provides context for changes

### write_to_file
```
<write_to_file>
<path>src/main.js</path>
<content>
// Your file content