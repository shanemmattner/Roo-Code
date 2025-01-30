# Model Context Protocol (MCP) Guide

The Model Context Protocol (MCP) is a powerful feature that enables Roo Code to extend its capabilities through custom tools and resources. This guide covers everything from basic concepts to advanced workflows.

## Understanding MCP

### What is MCP?
- Protocol for AI-tool communication
- Enables custom tool creation
- Provides resource access
- Extends Roo Code's capabilities

### Key Concepts
1. MCP Servers
   - Independent tool providers
   - Resource containers
   - API integrations
   - Custom functionality

2. Tools
   - Executable actions
   - Custom operations
   - API integrations
   - Workflow automation

3. Resources
   - Data sources
   - File access
   - Context providers
   - Information repositories

## Getting Started with MCP

### Basic Setup
1. MCP Configuration
   ```json
   {
     "mcpServers": {
       "weather": {
         "command": "node",
         "args": ["/path/to/weather-server/index.js"],
         "env": {
           "API_KEY": "your-key-here"
         }
       }
     }
   }
   ```

2. Server Management
   - Enable/disable servers
   - Configure timeouts
   - Set environment variables
   - Manage permissions

### Creating MCP Servers

#### Basic Server Structure
```typescript
#!/usr/bin/env node
import { Server } from '@modelcontextprotocol/sdk/server';
import { StdioServerTransport } from '@modelcontextprotocol/sdk/server/stdio';

class CustomServer {
  private server: Server;

  constructor() {
    this.server = new Server(
      {
        name: 'custom-server',
        version: '1.0.0'
      },
      {
        capabilities: {
          tools: {},
          resources: {}
        }
      }
    );
  }

  async run() {
    const transport = new StdioServerTransport();
    await this.server.connect(transport);
  }
}
```

#### Adding Tools
```typescript
this.server.setRequestHandler(CallToolRequestSchema, async (request) => {
  // Tool implementation
});
```

#### Adding Resources
```typescript
this.server.setRequestHandler(ReadResourceRequestSchema, async (request) => {
  // Resource implementation
});
```

## Using MCP Tools

### Tool Invocation
```
User: Use the weather tool to check San Francisco
Roo: I'll use the weather MCP tool:
<use_mcp_tool>
<server_name>weather</server_name>
<tool_name>get_forecast</tool_name>
<arguments>
{
  "city": "San Francisco",
  "days": 5
}
</arguments>
</use_mcp_tool>
```

### Resource Access
```
User: Get the latest documentation
Roo: I'll access the docs resource:
<access_mcp_resource>
<server_name>docs</server_name>
<uri>docs://api/latest</uri>
</access_mcp_resource>
```

## Advanced MCP Features

### Auto-Approval
- Configure trusted tools
- Set operation limits
- Define allowed patterns
- Manage permissions

### Network Configuration
```json
{
  "mcpServers": {
    "custom-server": {
      "networkTimeout": 3600,
      "retryAttempts": 3
    }
  }
}
```

### Tool Restrictions
```json
{
  "toolRestrictions": {
    "patterns": [
      "safe-operation-*",
      "read-only-*"
    ]
  }
}
```

## Common MCP Use Cases

### 1. API Integration
```typescript
// GitHub API integration
class GitHubServer {
  async getPullRequests() {
    // Implementation
  }

  async createIssue() {
    // Implementation
  }
}
```

### 2. Data Processing
```typescript
// Data processing tool
class DataProcessor {
  async analyzeData() {
    // Implementation
  }

  async generateReport() {
    // Implementation
  }
}
```

### 3. External Services
```typescript
// Weather service integration
class WeatherService {
  async getForecast() {
    // Implementation
  }

  async getAlerts() {
    // Implementation
  }
}
```

## Best Practices

### Server Development
1. Error Handling
   ```typescript
   try {
     // Operation
   } catch (error) {
     throw new McpError(
       ErrorCode.InternalError,
       `Operation failed: ${error.message}`
     );
   }
   ```

2. Resource Management
   ```typescript
   class ResourceManager {
     cleanup() {
       // Resource cleanup
     }
   }
   ```

3. Security Considerations
   - Validate inputs
   - Sanitize outputs
   - Manage credentials
   - Control access

### Tool Design
1. Clear Interfaces
   ```typescript
   interface ToolConfig {
     name: string;
     description: string;
     inputSchema: object;
   }
   ```

2. Proper Documentation
   ```typescript
   /**
    * @description Fetches weather data
    * @param {string} location - City name
    * @returns {Promise<WeatherData>}
    */
   ```

3. Version Management
   ```typescript
   const VERSION = '1.0.0';
   const API_VERSION = 'v1';
   ```

## Troubleshooting

### Common Issues
1. Connection Problems
   - Check network settings
   - Verify server status
   - Confirm credentials

2. Tool Failures
   - Review error logs
   - Check input validation
   - Verify API status

3. Resource Issues
   - Validate URIs
   - Check permissions
   - Verify data format

## Next Steps

1. Explore [Custom Modes](custom-modes.md) for MCP integration
2. Learn about [Adaptive Autonomy](adaptive-autonomy.md)
3. Master [Context Mentions](context-mentions.md)
4. Join our [Discord](https://discord.gg/roocode) for MCP tips