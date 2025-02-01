---
title: Roo Agent Modes
layout: page
nav_order: 6
has_children: true
---

# Roo Agent Modes

## Default Modes

### Core Modes Overview
- **Code Mode**: Advanced code generation and editing
- **Architect Mode**: System design and high-level technical guidance
- **Ask Mode**: Technical information and Q&A assistance
- **Design Mode**: UI/UX and design system development

## Custom Modes

### Creating Custom Modes
- Define unique mode characteristics
- Specify tool group access
- Configure mode-specific instructions

#### Custom Mode Structure
```json
{
  "slug": "designer",
  "name": "Designer",
  "roleDefinition": "UI/UX expert specializing in design systems",
  "groups": [
    "read",
    "edit",
    "browser"
  ],
  "customInstructions": "Focus on design consistency and user experience"
}
```

### Mode-Specific Instructions

#### Master Instructions
- Define core behavior
- Set context and capabilities
- Establish mode boundaries

##### Mode Specific Details
- Unique prompt templates
- Specialized tool access
- Contextual understanding

## Mode Switching

### Dynamic Mode Management
- Seamless transitions between modes
- Context preservation
- Intelligent mode recommendation

## Best Practices
- Choose the right mode for your task
- Leverage mode-specific capabilities
- Experiment with custom mode configurations
- Regularly update mode definitions