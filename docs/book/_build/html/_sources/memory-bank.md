# Memory Bank

The Memory Bank is a powerful feature that helps Roo Code maintain context and knowledge across sessions. It serves as a persistent memory system that can be updated and referenced to maintain continuity in long-running or complex tasks.

## Understanding Memory Bank

### Purpose
- Preserves important context across memory resets
- Documents current state and progress
- Maintains clear next steps
- Ensures task continuity

### When to Use
Memory Bank updates are particularly useful when:
1. Working on complex, multi-stage projects
2. Handling tasks that span multiple sessions
3. Needing to preserve context for future reference
4. Documenting critical decision points

## Using Memory Bank

### Triggering Updates
To update the Memory Bank, simply type:
```
update memory bank
```

This command signals Roo Code to:
1. Document everything about the current state
2. Make next steps crystal clear
3. Complete the current task
4. Prepare for potential memory reset

### Best Practices

#### What to Include
1. Current Project State
   - Progress made
   - Decisions taken
   - Problems encountered
   - Solutions implemented

2. Context Information
   - Project requirements
   - Technical constraints
   - Important dependencies
   - Environment details

3. Next Steps
   - Pending tasks
   - Known issues
   - Future considerations
   - Required follow-ups

#### When to Update
1. Before Complex Operations
   - Before major refactoring
   - Prior to system architecture changes
   - When switching between major features

2. At Milestone Completion
   - After implementing key features
   - When reaching project checkpoints
   - Upon resolving critical issues

3. During Long Sessions
   - When context becomes complex
   - Before taking breaks
   - When switching focus areas

## Memory Bank Structure

### Components

1. State Documentation
```json
{
  "currentState": {
    "completedTasks": [],
    "activeChanges": {},
    "environmentState": {}
  }
}
```

2. Context Preservation
```json
{
  "context": {
    "projectRequirements": [],
    "technicalDecisions": [],
    "dependencies": []
  }
}
```

3. Next Steps
```json
{
  "nextSteps": {
    "immediate": [],
    "planned": [],
    "considerations": []
  }
}
```

## Integration with Other Features

### Custom Modes
- Each mode can maintain its own memory context
- Mode-specific information is preserved
- Transitions between modes are documented

### Project Documentation
- Memory Bank updates can be used to generate documentation
- Key decisions are tracked and explained
- Project evolution is recorded

### Task Management
- Tracks task dependencies
- Maintains progress status
- Documents blockers and solutions

## Best Practices

### Documentation Quality
1. Be Specific
   - Include concrete details
   - Document exact steps taken
   - Record specific versions and configurations

2. Maintain Context
   - Explain why decisions were made
   - Document dependencies
   - Note any assumptions

3. Plan Ahead
   - Outline next steps clearly
   - Identify potential challenges
   - List required resources

### Organization Tips
1. Use Clear Categories
   - Separate technical and business context
   - Group related information
   - Maintain chronological order

2. Regular Updates
   - Schedule periodic updates
   - Update after major changes
   - Document incremental progress

3. Clean Structure
   - Use consistent formatting
   - Include timestamps
   - Reference related documents

## Example Usage

### Basic Update
```
User: update memory bank
Roo: Documenting current state:
- Implemented user authentication
- Set up database schema
- Created API endpoints

Next steps:
1. Implement input validation
2. Add error handling
3. Write unit tests
```

### Complex Project
```
User: update memory bank
Roo: Current State:
- Microservice architecture defined
- Service boundaries established
- Communication protocols selected

Technical Context:
- Using gRPC for inter-service communication
- PostgreSQL for persistent storage
- Redis for caching

Next Phase:
1. Implement service discovery
2. Set up monitoring
3. Deploy initial services
```

## Next Steps

1. Learn about [Custom Modes](custom-modes.md) for role-specific memory
2. Explore [Context Mentions](context-mentions.md) for enhanced context
3. Understand [Adaptive Autonomy](adaptive-autonomy.md) settings
4. Join our [Discord](https://discord.gg/roocode) for memory management tips