# Custom Modes

Custom Modes allow you to shape Roo Code's behavior, expertise, and capabilities to match specific roles in your development workflow. This powerful feature enables you to create specialized AI assistants tailored to your needs.

## Built-in Modes

### Code Mode
- Default coding assistant
- Full access to all tools
- Focus on implementation
- Example tasks:
  * Writing code
  * Debugging
  * Testing
  * File operations

### Architect Mode
- System design expert
- Limited to markdown editing
- Focus on planning and architecture
- Example tasks:
  * System design
  * Pattern recommendations
  * Architecture reviews
  * Technical documentation

### Ask Mode
- Technical research assistant
- Limited to markdown editing
- Focus on knowledge sharing
- Example tasks:
  * Code explanation
  * Best practices
  * Technology comparison
  * Documentation help

## Creating Custom Modes

### Basic Creation
1. Type in chat: "Create a new mode for X"
2. Or manually create in settings:
   ```json
   {
     "customModes": [
       {
         "slug": "qa-engineer",
         "name": "QA Engineer",
         "roleDefinition": "You are Roo, a QA expert...",
         "groups": ["read", "edit", "browser"]
       }
     ]
   }
   ```

### Mode Components

#### Required Fields
- `slug`: Unique identifier (lowercase, hyphens)
- `name`: Display name
- `roleDefinition`: Detailed role description
- `groups`: Allowed tool groups

#### Optional Fields
- `customInstructions`: Additional behavior guidelines
- `fileRestrictions`: File access patterns
- `autoApproveSettings`: Default autonomy levels

### Tool Groups
Available groups:
- `read`: File reading and searching
- `edit`: File creation and modification
- `browser`: Browser automation
- `command`: Terminal operations
- `mcp`: Model Context Protocol tools

## File Restrictions

### Pattern-Based Access
```json
{
  "fileRestrictions": {
    "patterns": [
      {
        "regex": "\\.test\\.ts$",
        "description": "TypeScript test files"
      },
      {
        "regex": "\\.md$",
        "description": "Markdown files"
      }
    ]
  }
}
```

### Common Patterns
- Test files: `\\.test\\.[jt]s$`
- Documentation: `\\.md$`
- Styles: `\\.css$`
- Configuration: `\\.json$`

## Example Modes

### QA Engineer
```json
{
  "slug": "qa-engineer",
  "name": "QA Engineer",
  "roleDefinition": "You are Roo, a QA expert specializing in test automation, quality assurance, and bug detection...",
  "groups": ["read", "edit", "browser"],
  "fileRestrictions": {
    "patterns": [
      {
        "regex": "\\.test\\.[jt]s$",
        "description": "Test files"
      },
      {
        "regex": "\\.spec\\.[jt]s$",
        "description": "Spec files"
      }
    ]
  }
}
```

### Technical Writer
```json
{
  "slug": "tech-writer",
  "name": "Technical Writer",
  "roleDefinition": "You are Roo, a technical writing expert focused on clear, accurate documentation...",
  "groups": ["read", "edit"],
  "fileRestrictions": {
    "patterns": [
      {
        "regex": "\\.md$",
        "description": "Markdown files"
      },
      {
        "regex": "\\.rst$",
        "description": "ReStructuredText files"
      }
    ]
  }
}
```

### DevOps Engineer
```json
{
  "slug": "devops",
  "name": "DevOps Engineer",
  "roleDefinition": "You are Roo, a DevOps expert specializing in automation, deployment, and infrastructure...",
  "groups": ["read", "edit", "command"],
  "fileRestrictions": {
    "patterns": [
      {
        "regex": "Dockerfile$",
        "description": "Docker files"
      },
      {
        "regex": "\\.ya?ml$",
        "description": "YAML files"
      }
    ]
  }
}
```

## Mode Switching

### Manual Switching
- Use mode dropdown in chat
- Command palette command
- Mode-specific keyboard shortcuts

### Automatic Switching
Modes can request switches based on context:
```json
{
  "allowedTransitions": {
    "architect": ["code", "qa-engineer"],
    "code": ["test-engineer", "devops"]
  }
}
```

## Best Practices

### Role Definition
1. Be specific about expertise
2. Define clear boundaries
3. Include example tasks
4. Specify communication style

### Tool Access
1. Limit to necessary groups
2. Use specific file patterns
3. Consider security implications
4. Document restrictions

### Mode Organization
1. Group related modes
2. Establish clear hierarchies
3. Define transition paths
4. Document relationships

## Sharing Modes

### Export Format
```json
{
  "mode": {
    "slug": "your-mode",
    "name": "Your Mode",
    "roleDefinition": "...",
    "groups": [],
    "fileRestrictions": {}
  }
}
```

### Community Resources
- Share on Discord
- Post to Reddit
- GitHub discussions
- Mode registry (coming soon)

## Next Steps

1. Explore [API Model Support](api-model-support.md) for mode-specific models
2. Learn about [Adaptive Autonomy](adaptive-autonomy.md) per mode
3. Understand [File Operations](file-operations.md) restrictions
4. Join our [Discord](https://discord.gg/roocode) to share modes