# API and Model Support

Roo Code supports a wide range of AI providers and models, allowing you to choose the best option for your needs. This flexibility enables you to optimize for cost, performance, or specific capabilities.

## Supported Providers

### OpenRouter
- Access to multiple models through a single API
- Usage tracking and cost management
- Simplified model switching

### Anthropic
- Claude models
- Strong reasoning capabilities
- Extensive context window

### OpenAI
- GPT-4 and GPT-3.5 models
- Consistent performance
- Wide compatibility

### Google Gemini
- Advanced multimodal capabilities
- Competitive pricing
- Strong technical understanding

### AWS Bedrock
- Multiple model options
- Enterprise-grade reliability
- AWS integration

### Azure OpenAI
- Enterprise security
- Regional deployment options
- Azure integration

### GCP Vertex
- Google Cloud integration
- Enterprise features
- Scalable deployment

### Local Models
#### LM Studio
- Run models locally
- Privacy-focused
- Customizable deployment

#### Ollama
- Easy local deployment
- Multiple model support
- Command-line integration

## Configuration

### Setting Up Providers
1. Access Roo Code settings
2. Navigate to API Configuration
3. Add provider credentials:
   ```json
   {
     "provider": "openai",
     "apiKey": "your-api-key",
     "model": "gpt-4"
   }
   ```

### Multiple Configurations
Configure different providers for different modes:
```json
{
  "profiles": {
    "code": {
      "provider": "anthropic",
      "model": "claude-2"
    },
    "architect": {
      "provider": "openai",
      "model": "gpt-4"
    }
  }
}
```

## Usage Tracking

### Monitoring
- Token usage per session
- Cost tracking
- Usage patterns
- Rate limiting status

### Cost Management
1. Set usage limits
2. Monitor costs
3. Optimize model selection
4. Track per-mode usage

## Best Practices

### Model Selection

#### Code Mode
- Optimize for:
  * Code understanding
  * Fast response time
  * Cost efficiency
- Recommended models:
  * Claude-instant
  * GPT-3.5-turbo
  * Local models

#### Architect Mode
- Optimize for:
  * Deep reasoning
  * System design
  * Pattern recognition
- Recommended models:
  * GPT-4
  * Claude-2
  * Gemini Pro

#### Ask Mode
- Optimize for:
  * Knowledge breadth
  * Explanation clarity
  * Documentation
- Recommended models:
  * GPT-4
  * Claude-2
  * Gemini Pro

### Cost Optimization
1. Use faster models for routine tasks
2. Reserve advanced models for complex work
3. Leverage local models when possible
4. Monitor and adjust based on usage patterns

## Provider-Specific Features

### OpenRouter
- Model comparison
- Automatic fallback
- Usage analytics
- Cost optimization

### Anthropic
- Constitutional AI
- Improved safety
- Ethical considerations
- Extended context

### OpenAI
- Function calling
- Tool use
- System messages
- Response streaming

### Local Models
- Complete privacy
- No internet requirement
- Customizable models
- Lower latency

## Troubleshooting

### Common Issues
1. API Connection
   - Check API keys
   - Verify network connection
   - Confirm rate limits

2. Model Availability
   - Check provider status
   - Verify model access
   - Confirm quota availability

3. Performance
   - Monitor response times
   - Check resource usage
   - Optimize prompt length

### Getting Help
- Provider documentation
- Roo Code Discord
- GitHub issues
- Reddit community

## Next Steps

1. Explore [Custom Modes](custom-modes.md) for mode-specific configurations
2. Learn about [Context Mentions](context-mentions.md) for efficient prompting
3. Understand [Adaptive Autonomy](adaptive-autonomy.md) settings
4. Join our [Discord](https://discord.gg/roocode) for provider-specific tips