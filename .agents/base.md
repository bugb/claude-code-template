# Overview
This document provides a structural overview of the learning-hub project, designed to aid AI code assistants (like Copilot, Claude Code) in understanding the codebase.

Please refer to README.md for a complete and up-to-date project overview, and CONTRIBUTING.md for implementation guidelines and contribution procedures.

# Topic-Specific Instructions

**IMPORTANT**: When working on files in specific learning modules, ALWAYS read the local CLAUDE.md file first for topic-specific guidelines:

- **HTML work** (files in `frontend/core/html/`): Read `frontend/core/html/CLAUDE.md`
- **CSS work** (files in `frontend/core/css/`): Read `frontend/core/css/CLAUDE.md` 
- **JavaScript work** (files in `frontend/core/javascript/`): Read `frontend/core/javascript/CLAUDE.md`
- **Node.js work** (files in `backend/nodejs/`): Read `backend/nodejs/CLAUDE.md`
- **AI work** (files in `ai/`): Read `ai/CLAUDE.md`
- **DevOps work** (files in `devops/`): Read `devops/CLAUDE.md`

These topic-specific files contain:
- Module-specific standards and requirements
- Demo/example structure guidelines
- Content formatting rules
- Educational approach for that topic
- Quality standards and best practices

**Priority order**: Topic-specific CLAUDE.md → .agents/base.md → root CLAUDE.md

# Project Structure
The project is organized into the following directories:

learning-hub/
├── ai/ # AI source code
├── backend / # Frontend source code
│   └── nodejs / # Nodejs
├── devops / # Devops source code
├── frontend / # Frontend source code
│   ├── core/ # Core logic of Repomix
│   │   ├── css/ # CSS basic
│   │   ├── html/ # HTML basic
│   │   └── javascript/ # JS basic
│   ├── react/ # Core logic of Repomix
│   │   ├── official-docs/ # Learn the basics of React from the official doc
│   │   └── course-a/ # Learn the basics of React from course-a
└── ...

# Generate Comprehensive Output
- Include all content without abbreviation, unless specified otherwise
- Optimize for handling large codebases while maintaining output quality
- GitHub Release Note Guidelines

# When writing release notes, please follow these guidelines:

- When referencing issues or PRs, use the gh command to verify the content:
```
gh issue view <issue-number>  # For checking issue content
gh pr view <pr-number>        # For checking PR content
```
This helps ensure accuracy in release note descriptions.
Please retrieve and reference the latest release notes from .github/releases/ as they contain past release examples.


# Git Instructions
- @~/.agents/rules/git-instructions.md

# General Coding guidelines
- @~/.agents/rules/general-coding-guidelines.md

# PR review guidelines
- @~/.agents/rules/pr-review-guidelines.md
