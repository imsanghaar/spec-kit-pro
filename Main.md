# SpeckitPro: Comprehensive Guide

## Table of Contents

1. [Introduction](#introduction)
2. [Core Philosophy](#core-philosophy)
3. [Installation](#installation)
4. [Basic Usage](#basic-usage)
5. [Commands Reference](#commands-reference)
6. [AI Agent Integration](#ai-agent-integration)
7. [Project Structure](#project-structure)
8. [Workflow Examples](#workflow-examples)
9. [Best Practices](#best-practices)
10. [Troubleshooting](#troubleshooting)

## Introduction

SpeckitPro (formerly SpecifyPro) is a powerful command-line interface tool that enables **Spec-Driven Development** methodology. It combines the rapid, conversational generation power of "vibe coding" with the structure and architectural coherence provided by the "spec-driven" methodology.

The tool is designed to help developers focus on product scenarios and predictable outcomes instead of coding every piece from scratch. It provides a structured workflow for developing scalable, multi-agent AI systems using patterns, templates, and reference projects.

### Key Features

- **Spec-Driven Development**: Specifications become executable, directly generating working implementations
- **AI Agent Integration**: Works seamlessly with multiple AI coding agents
- **Structured Workflow**: Five-step process from constitution to implementation
- **Template System**: Pre-built templates for various AI agents and technologies
- **Version Control**: Integrated Git support and branching strategies

## Core Philosophy

### Spec-Driven Development Flips the Script

For decades, code has been king — specifications were just scaffolding we built and discarded once the "real work" of coding began. SpeckitPro changes this: **specifications become executable**, directly generating working implementations rather than just guiding them.

### The Five-Step Development Process

1. **Constitution** → Establish project principles and development guidelines
2. **Specify** → Define what you want to build (requirements and user stories)
3. **Plan** → Create technical implementation plans with your chosen tech stack
4. **Tasks** → Generate actionable task lists for implementation
5. **Implement** → Execute all tasks to build your feature according to the plan

## Installation

### Prerequisites

- **Operating System**: Linux/macOS/Windows
- **Python**: 3.11 or higher
- **Git**: Version control system
- **uv**: Package manager (recommended)

### Installation Methods

#### Option 1: Persistent Installation (Recommended)

```bash
# From PyPI (recommended)
pip install specifypro

# Or with uv tools
uv tool install specifypro

# Upgrade to latest later
pip install -U specifypro
uv tool upgrade specifypro
```

#### Option 2: One-time Usage

```bash
uvx specifypro --help
uvx specifypro init <PROJECT_NAME>
# or
uvx spp init <PROJECT_NAME>
```

### Uninstall

```bash
pip uninstall specifypro
# or
uv tool uninstall specifypro
```

## Basic Usage

### Creating a New Project

```bash
# Using the main command
specifypro init my-project
# or using the alias
spp init my-project
```

### Initializing with Specific AI Assistant

```bash
# With Claude Code
specifypro init my-project --ai claude
spp init my-project --ai claude

# With GitHub Copilot
specifypro init my-project --ai copilot
spp init my-project --ai copilot

# With Cursor
specifypro init my-project --ai cursor
spp init my-project --ai cursor

# With Qoder
specifypro init my-project --ai qoder
spp init my-project --ai qoder

# With IBM Bob
specifypro init my-project --ai bob
spp init my-project --ai bob

# With SHAI
specifypro init my-project --ai shai
spp init my-project --ai shai

# With Amp
specifypro init my-project --ai amp
spp init my-project --ai amp

# With Windsurf
specifypro init my-project --ai windsurf
spp init my-project --ai windsurf
```

### Advanced Initialization Options

```bash
# Initialize in current directory
specifypro init . --ai claude
spp init . --ai claude

# Initialize with PowerShell scripts (Windows)
specifypro init my-project --ai copilot --script ps
spp init my-project --ai copilot --script ps

# Skip git initialization
specifypro init my-project --ai gemini --no-git
spp init my-project --ai gemini --no-git

# Enable debug output
specifypro init my-project --ai claude --debug
spp init my-project --ai claude --debug

# Use GitHub token for API requests
specifypro init my-project --ai claude --github-token ghp_your_token_here
spp init my-project --ai claude --github-token ghp_your_token_here

# Force merge into current directory without confirmation
specifypro init . --force --ai copilot
spp init . --force --ai copilot
```

### Check System Requirements

```bash
specifypro check
spp check
```

### Check Version

```bash
specifypro --version
spp --version
specifypro -v
spp -v
```

## Commands Reference

### Main Commands

#### `init` - Initialize New Projects

Initialize a new SpeckitPro project from the latest template.

**Arguments & Options:**

- `<project-name>`: Name for your new project directory (optional if using `--here`, or use `.` for current directory)
- `--ai`: AI assistant to use: `claude`, `gemini`, `copilot`, `cursor`, `qwen`, `opencode`, `codex`, `windsurf`, `kilocode`, `auggie`, `roo`, `codebuddy`, `amp`, `shai`, `q`, `bob`, or `qoder`
- `--script`: Script type to use: `sh` (bash/zsh) or `ps` (PowerShell)
- `--ignore-agent-tools`: Skip checks for AI agent tools like Claude Code
- `--no-git`: Skip git repository initialization
- `--here`: Initialize project in the current directory instead of creating a new one
- `--force`: Force merge/overwrite when initializing in current directory (skip confirmation)
- `--skip-tls`: Skip SSL/TLS verification (not recommended)
- `--debug`: Enable detailed debug output for troubleshooting
- `--github-token`: GitHub token for API requests (or set GH_TOKEN/GITHUB_TOKEN env variable)

**Examples:**

```bash
# Basic project initialization
specifypro init my-project
spp init my-project

# Initialize with specific AI assistant
specifypro init my-project --ai claude
spp init my-project --ai claude

# Initialize in current directory
specifypro init . --ai copilot
spp init . --ai copilot

# Skip git initialization
specifypro init my-project --ai gemini --no-git
spp init my-project --ai gemini --no-git
```

#### `check` - Check System Requirements

Check that all required tools are installed.

**Examples:**

```bash
specifypro check
spp check
```

#### `version` - Display Version Information

Display version and system information.

**Examples:**

```bash
specifypro --version
spp --version
specifypro -v
spp -v
```

### AI Agent Commands (Slash Commands)

Once you run `specifypro init`, your AI coding agent will have access to these slash commands for structured development:

#### Core Commands

##### `/spp.constitution` - Establish Project Principles

Create or update project governing principles and development guidelines that will guide all subsequent development.

**Usage:**

```markdown
/spp.constitution Create principles focused on code quality, testing standards, user experience consistency, and performance requirements
```

##### `/spp.specify` - Define Requirements

Define what you want to build (requirements and user stories). Focus on the "what" and "why", not the tech stack.

**Usage:**

```markdown
/spp.specify Build an application that can help me organize my photos in separate photo albums. Albums are grouped by date and can be re-organized by dragging and dropping on the main page. Albums are never in other nested albums. Within each album, photos are previewed in a tile-like interface.
```

##### `/spp.plan` - Create Technical Plan

Create technical implementation plans with your chosen tech stack and architecture choices.

**Usage:**

```markdown
/spp.plan The application uses Vite with minimal number of libraries. Use vanilla HTML, CSS, and JavaScript as much as possible. Images are not uploaded anywhere and metadata is stored in a local SQLite database.
```

##### `/spp.tasks` - Generate Actionable Tasks

Generate actionable task lists for implementation.

**Usage:**

```markdown
/spp.tasks
```

##### `/spp.implement` - Execute Implementation

Execute all tasks to build your feature according to the plan.

**Usage:**

```markdown
/spp.implement
```

#### Optional Commands

##### `/spp.clarify` - Clarify Specifications

Clarify underspecified areas (recommended before `/spp.plan`; formerly `/quizme`).

**Usage:**

```markdown
/spp.clarify Focus on security and performance requirements.
```

##### `/spp.analyze` - Cross-Artifact Analysis

Cross-artifact consistency & coverage analysis (run after `/spp.tasks`, before `/spp.implement`).

**Usage:**

```markdown
/spp.analyze
```

##### `/spp.checklist` - Generate Quality Checklists

Generate custom quality checklists that validate requirements completeness, clarity, and consistency (like "unit tests for English").

**Usage:**

```markdown
/spp.checklist
```

## AI Agent Integration

SpeckitPro integrates with multiple AI agents to enhance your development workflow:

### Supported AI Agents

| Agent | Support | Notes |
| --- | --- | --- |
| Qoder CLI | ✅ | |
| Amazon Q Developer CLI | ⚠️ | Does not support custom arguments for slash commands |
| Amp | ✅ | |
| Auggie CLI | ✅ | |
| Claude Code | ✅ | |
| CodeBuddy CLI | ✅ | |
| Codex CLI | ✅ | |
| Cursor | ✅ | |
| Gemini CLI | ✅ | |
| GitHub Copilot | ✅ | |
| IBM Bob | ✅ | IDE-based agent with slash command support |
| Jules | ✅ | |
| Kilo Code | ✅ | |
| opencode | ✅ | |
| Qwen Code | ✅ | |
| Roo Code | ✅ | |
| SHAI (OVHcloud) | ✅ | |
| Windsurf | ✅ | |

### Setting Up AI Agents

Each AI agent requires specific setup and configuration. SpeckitPro will check if the required tools are installed when you initialize a project with a specific AI assistant.

## Project Structure

When you initialize a SpeckitPro project, it creates the following structure:

```text
my-project/
├── .specify/
│   ├── memory/
│   │   └── constitution.md
│   ├── scripts/
│   │   ├── check-prerequisites.sh
│   │   ├── common.sh
│   │   ├── create-new-feature.sh
│   │   ├── setup-plan.sh
│   │   └── update-claude-md.sh
│   ├── specs/
│   │   └── [feature-name]/
│   │       └── spec.md
│   └── templates/
│       ├── plan-template.md
│       ├── spec-template.md
│       └── tasks-template.md
├── .git/
├── .gitignore
└── README.md
```

### Key Directories

- **`.specify/memory/`**: Contains project constitution and principles
- **`.specify/scripts/`**: Automation scripts for various tasks
- **`.specify/specs/`**: Feature specifications organized by feature
- **`.specify/templates/`**: Template files for various documentation

## Workflow Examples

### Complete Development Workflow

1. **Initialize Project**

   ```bash
   specifypro init my-awesome-app --ai claude
   cd my-awesome-app
   ```

2. **Establish Project Principles**

   ```text
   /spp.constitution Create principles focused on code quality, testing standards, user experience consistency, and performance requirements
   ```

3. **Define Specifications**

   ```text
   /spp.specify Build a task management application with user authentication, project organization, and collaboration features
   ```

4. **Clarify Specifications** (Optional but Recommended)

   ```text
   /spp.clarify Focus on security requirements and data privacy compliance
   ```

5. **Create Technical Plan**

   ```text
   /spp.plan Use React for frontend, Node.js/Express for backend, MongoDB for database, and implement JWT authentication
   ```

6. **Generate Tasks**

   ```text
   /spp.tasks
   ```

7. **Analyze Consistency** (Optional)

   ```text
   /spp.analyze
   ```

8. **Execute Implementation**

   ```text
   /spp.implement
   ```

### Iterative Development

For ongoing feature development, you can use the same workflow:

1. **Update Constitution** (if needed)

   ```text
   /spp.constitution Add principles for accessibility compliance
   ```

2. **Add New Feature**

   ```text
   /spp.specify Implement dark mode support for the application
   ```

3. **Plan Implementation**

   ```text
   /spp.plan Use CSS variables for theme management and localStorage for preference persistence
   ```

4. **Generate and Execute Tasks**

   ```text
   /spp.tasks
   /spp.implement
   ```

## Best Practices

### 1. Start with Strong Principles

Always establish clear project principles with `/spp.constitution` before beginning development. These principles will guide all subsequent decisions.

### 2. Be Specific in Specifications

When using `/spp.specify`, focus on the "what" and "why" rather than implementation details. Be as specific as possible about user needs and requirements.

### 3. Clarify Before Planning

Use `/spp.clarify` before `/spp.plan` to resolve ambiguities and ensure clear requirements before committing to technical decisions.

### 4. Plan Before Implementing

Always create a technical plan with `/spp.plan` before implementing to ensure architectural coherence and consistency.

### 5. Generate Tasks Before Implementation

Use `/spp.tasks` to break down the implementation into manageable, actionable steps before running `/spp.implement`.

### 6. Use Analysis for Quality

Run `/spp.analyze` after tasks generation to identify consistency issues and improve quality before implementation.

### 7. Generate Checklists for Validation

Use `/spp.checklist` to create quality validation criteria that ensure requirements completeness and clarity.

### 8. Iterate in Small Steps

Break large features into smaller, manageable chunks and use the workflow for each iteration.

## Troubleshooting

### Common Issues and Solutions

#### Issue: AI Agent Not Found

**Problem**: SpeckitPro reports that your AI agent is not installed.
**Solution**: Install the required AI agent CLI tool or use the `--ignore-agent-tools` flag during initialization.

#### Issue: Network Connection Problems

**Problem**: SpeckitPro fails to download templates due to network issues.
**Solution**: Use the `--debug` flag to get more information about the connection issue.

#### Issue: Git Not Initialized

**Problem**: Git repository is not created during project initialization.
**Solution**: Ensure Git is installed and in your PATH, or use the `--no-git` flag to skip git initialization.

#### Issue: SSL/TLS Verification Errors

**Problem**: SSL/TLS certificate verification fails during template downloads.
**Solution**: Use the `--skip-tls` flag to skip SSL verification (not recommended for production).

#### Issue: Permission Denied

**Problem**: SpeckitPro fails to create or modify files due to permission issues.
**Solution**: Ensure you have write permissions to the target directory and run with appropriate privileges.

### Debugging Commands

Use the `--debug` flag with any SpeckitPro command to get more detailed output:

```bash
specifypro init my-project --ai claude --debug
spp init my-project --ai claude --debug
```

### Version Information

Check your SpeckitPro version and system information:

```bash
specifypro --version
spp --version
specifypro -v
spp -v
```

### Check Dependencies

Verify that required tools are installed:

```bash
specifypro check
spp check
```

## Environment Variables

SpeckitPro recognizes the following environment variables:

- `SPECIFY_FEATURE`: Override feature detection for non-Git repositories. Set to the feature directory name (e.g., `001-photo-albums`) to work on a specific feature when not using Git branches.

## Conclusion

SpeckitPro is a powerful tool that bridges the gap between rapid development ("vibe coding") and structured, predictable outcomes ("spec-driven development"). By following the five-step workflow and using the slash commands with your AI agent, you can build scalable, maintainable applications with clear principles and requirements.

The key to success with SpeckitPro is to embrace the structured approach while leveraging the creative power of AI agents. Start with strong principles, clearly define your specifications, plan thoughtfully, break down tasks systematically, and implement with confidence.

Happy coding with SpeckitPro!
