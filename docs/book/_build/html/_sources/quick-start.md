# Quick Start Guide

This guide will help you get up and running with Roo Code quickly, demonstrating basic usage patterns and common workflows. For detailed installation instructions, see the [Installation Guide](installation.md).

## Basic Interaction

### Starting a Conversation
1. Open Roo Code in VS Code
2. Type your request in natural language
3. Roo Code will:
   - Analyze your request
   - Propose actions
   - Execute them upon approval

### Example Interactions

#### Creating a New File
```
User: Create a simple HTML file with a heading and paragraph
Roo: I'll create an index.html file with basic HTML structure. Here's what I'll do:
[Roo shows file content and waits for approval]
[After approval, creates the file]
```

#### Modifying Existing Code
```
User: Add error handling to this function
Roo: I'll analyze the function and add try-catch blocks. Here's the proposed change:
[Roo shows diff and waits for approval]
[After approval, applies the changes]
```

## Working with Different Modes

### Code Mode (Default)
- General-purpose coding tasks
- [File operations](file-operations.md)
- Terminal commands
- Browser automation

Example:
```
User: Add input validation to the login form
Roo: I'll examine the form and add validation...
```

### Architect Mode
- System design discussions
- Architecture recommendations
- Best practices advice
- See [Structured Approach](structured-approach.md) for details

Example:
```
User: What's the best way to structure this microservice?
Roo: Let's analyze the requirements...
```

### Ask Mode
- Technical questions
- Documentation help
- Concept explanations
- See [Planning Guide](planning-guide.md) for effective usage

Example:
```
User: Explain how React hooks work
Roo: Hooks are a feature in React that...
```

## Common Tasks

### File Operations
See [File Operations](file-operations.md) for detailed information about:
- Create new files
- Modify existing files
- Search across files
- Analyze code structure

### Terminal Commands
- Run build commands
- Install dependencies
- Execute tests
- Start development servers

### Browser Automation
- Test web applications
- Verify changes
- Capture screenshots
- Monitor console logs

## Best Practices

### Writing Effective Prompts
1. Be specific about your goals
2. Provide context when needed
3. Use @file or @folder mentions for additional context
4. Break complex tasks into smaller steps

### Managing Autonomy
See [Adaptive Autonomy](adaptive-autonomy.md) for details about:
1. Starting with manual approval
2. Gradually enabling auto-approve for trusted operations
3. Maintaining control over critical actions

### Using Context Mentions
- @file: Include specific file content
- @folder: Share directory structure
- @problems: Reference workspace issues
- @url: Include external documentation
- @git: Share code history

## Tips and Tricks

### Efficiency Tips
1. Use appropriate [Custom Modes](custom-modes.md) for different tasks
2. Leverage [Memory Bank](memory-bank.md) for context
3. Combine context mentions for better results
4. Keep development servers running in background

### Common Patterns
1. Start with high-level design in Architect mode
2. Switch to Code mode for implementation
3. Use Ask mode for clarification
4. Return to Code mode for testing

## Next Steps

1. Explore [Adaptive Autonomy](adaptive-autonomy.md) for more control
2. Learn about [API and Model Support](api-model-support.md)
3. Master [MCP Guide](mcp-guide.md) for extensibility
4. Join our [Discord community](https://discord.gg/roocode) for tips and support

## See Also

- [Custom Modes](custom-modes.md) for specialized workflows
- [Memory Bank](memory-bank.md) for context management
- [Structured Approach](structured-approach.md) for development methodology
- [Planning Guide](planning-guide.md) for effective task management