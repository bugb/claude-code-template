# Commit Messages
- Follow the Conventional Commits specification for all commit messages
- Always include a scope in your commit messages
```
Format: type(scope): Description
```
# Examples:
```
- feat(cli): Add new --no-progress flag
- fix(security): Handle special characters in file paths
- docs(website): Update installation guide
- style(website): Update GitHub sponsor button color
- refactor(core): Split packager into smaller modules
- test(cli): Add tests for new CLI options
```
Types: feat, fix, docs, style, refactor, test, chore, etc.
Scope should indicate the affected part of the codebase (cli, core, website, security, etc.)
Description should be clear and concise in present tense
Description must start with a capital letter

# Commit Body Guidelines
Include context about what led to this commit
Describe the conversation or problem that motivated the change
This helps preserve the decision-making process for future reference