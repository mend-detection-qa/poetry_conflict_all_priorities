# Test Case: Poetry All Priorities Conflict

## Package Manager
Poetry

## Python Version Detection
- **Source**: .python-version (PRIORITY #1)
- **Expected Version**: 3.8.0
- **Conflicts**:
  - .tool-versions says 3.9.0 (PRIORITY #2 - IGNORED)
  - tool.poetry.dependencies.python says ^3.10 (PRIORITY #3 - IGNORED)

## Files Present
- .python-version - 3.8.0 (SHOULD WIN)
- .tool-versions - python 3.9.0 (SHOULD BE IGNORED)
- pyproject.toml - python = "^3.10" (SHOULD BE IGNORED)
- poetry.lock

## Test Purpose
Comprehensive priority test with all top 3 priority sources conflicting.
