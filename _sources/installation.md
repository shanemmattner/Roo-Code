# Installation Guide

This guide will walk you through the process of installing and configuring Roo Code in your development environment.

## Installation Methods

### VS Code Marketplace (Recommended)
1. Open VS Code
2. Click on the Extensions icon in the Activity Bar or press `Ctrl+Shift+X` (`Cmd+Shift+X` on macOS)
3. Search for "Roo Code"
4. Click "Install"

### Open-VSX Registry
For open-source editors that support Open-VSX:
1. Access your editor's extension marketplace
2. Search for "Roo Code"
3. Install from Open-VSX registry

### Manual Installation
If you prefer manual installation:
1. Download the `.vsix` file from:
   - [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=RooVeterinaryInc.roo-cline)
   - [Open-VSX Registry](https://open-vsx.org/extension/RooVeterinaryInc/roo-cline)
2. Drag and drop the `.vsix` file into your editor
3. Or install via command line:
   ```bash
   code --install-extension path/to/roo-code-version.vsix
   ```

## Initial Setup

### Opening Roo Code
There are two ways to open Roo Code:
1. Click the Roo Code icon in the Activity Bar
2. Use the Command Palette (`Cmd/Ctrl + Shift + P`):
   - Type "Roo Code: Open in New Tab"
   - This docks the AI assistant alongside your file explorer

### API Configuration
Roo Code supports various AI providers:
- OpenRouter
- Anthropic
- Glama
- OpenAI
- Google Gemini
- AWS Bedrock
- Azure
- GCP Vertex
- Local models (LM Studio/Ollama)

Configure your preferred provider in the settings:
1. Open Roo Code settings
2. Add your API credentials
3. Select default models for different modes

### Custom Modes Setup
To configure custom modes:
1. Open the Prompts tab
2. Create new modes or modify existing ones
3. Set role definitions and allowed tools
4. Configure file access patterns if needed

## Verification

To verify your installation:
1. Open Roo Code
2. Type a simple command like "Hello"
3. Confirm you receive a response
4. Try a basic file operation to test workspace access

## Troubleshooting

### Common Issues

1. **API Connection Problems**
   - Verify API keys are correctly entered
   - Check network connectivity
   - Ensure API endpoint is accessible

2. **Extension Not Loading**
   - Restart VS Code
   - Check VS Code version compatibility
   - Verify extension installation status

3. **File Access Issues**
   - Confirm workspace trust settings
   - Check file permissions
   - Verify workspace is open in editor

### Getting Help

If you encounter problems:
1. Check the [Discord community](https://discord.gg/roocode)
2. Visit [Reddit r/RooCode](https://www.reddit.com/r/RooCode/)
3. Submit issues on [GitHub](https://github.com/RooVetGit/Roo-Code/issues)

## Next Steps

After installation:
1. Follow the [Quick Start Guide](quick-start.md)
2. Explore [Adaptive Autonomy](adaptive-autonomy.md) settings
3. Learn about [Custom Modes](custom-modes.md)
4. Join the community on [Discord](https://discord.gg/roocode)