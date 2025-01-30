# Adaptive Autonomy

Roo Code's adaptive autonomy system allows you to control how independently it operates. This feature lets you balance efficiency with oversight, adapting to your comfort level and the complexity of tasks.

## Understanding Autonomy Levels

### Manual Approval (Default)
- Every action requires explicit approval
- Best for:
  * Learning how Roo Code works
  * Critical system changes
  * Complex refactoring
  * Production deployments

### Auto-Approve Mode
- Roo Code executes approved actions without confirmation
- Configurable per action type
- Useful for:
  * Routine file operations
  * Format fixes
  * Documentation updates
  * Test file creation

### Hybrid Approach
- Combine auto-approve for safe operations
- Maintain manual approval for critical actions
- Example configuration:
  * Auto-approve: File writes, linting fixes
  * Manual approval: Terminal commands, deployments

## Configuring Autonomy

### Global Settings
1. Access Roo Code settings
2. Navigate to Autonomy section
3. Configure default behavior:
   ```json
   {
     "autoApprove": {
       "fileWrites": false,
       "terminalCommands": false,
       "browserActions": false
     }
   }
   ```

### Per-Action Type Settings
Configure autonomy for specific actions:

#### File Operations
```json
{
  "fileWrites": {
    "enabled": true,
    "patterns": [
      "*.md",
      "*.test.ts"
    ]
  }
}
```

#### Terminal Commands
```json
{
  "terminalCommands": {
    "enabled": true,
    "allowList": [
      "npm run test",
      "npm run lint"
    ]
  }
}
```

#### Browser Actions
```json
{
  "browserActions": {
    "enabled": true,
    "allowedOrigins": [
      "localhost:3000"
    ]
  }
}
```

## Safety Features

### Action Review
- Clear preview of proposed changes
- Diff view for file modifications
- Command preview for terminal operations
- Screenshot preview for browser actions

### Rollback Options
- Editor timeline integration
- Revert capability for file changes
- Terminal command history
- Browser session logs

### Built-in Safeguards
1. Syntax validation before file writes
2. Command sanitization
3. Browser action boundaries
4. Resource usage limits

## Best Practices

### Starting Out
1. Begin with manual approval
2. Learn Roo Code's patterns
3. Identify routine operations
4. Gradually enable auto-approve

### Production Environments
1. Maintain strict approval for:
   - Database operations
   - Deployment commands
   - Configuration changes
   - Security-sensitive files

### Development Workflow
1. Auto-approve for:
   - Test file creation
   - Documentation updates
   - Style fixes
   - Local development tasks

### Team Settings
1. Establish shared guidelines
2. Document approved automations
3. Regular review of settings
4. Audit automated actions

## Common Scenarios

### Local Development
```json
{
  "fileWrites": {
    "enabled": true,
    "patterns": ["*.test.*", "*.md", "*.css"]
  },
  "terminalCommands": {
    "enabled": true,
    "allowList": ["npm run dev", "npm test"]
  }
}
```

### Documentation Work
```json
{
  "fileWrites": {
    "enabled": true,
    "patterns": ["*.md", "docs/*"]
  }
}
```

### Production Support
```json
{
  "autoApprove": false,
  "requireReview": true
}
```

## Next Steps

1. Explore [Custom Modes](custom-modes.md) for role-specific autonomy settings
2. Learn about [File Operations](file-operations.md) for detailed control
3. Understand [Command Line Integration](command-line.md) for terminal automation
4. Review [Browser Automation](browser-automation.md) capabilities