# Pull Request: Fix Development Environment Import Issues

## Description
This PR resolves the common "Import 'frappe' could not be resolved" error that developers encounter when working with ERPNext code. The solution provides comprehensive documentation and configuration files to help developers set up their development environment correctly.

## Root Cause
The error occurs because:
1. The `frappe` module is not a standard Python package
2. It's part of the Frappe Framework which needs to be installed separately
3. IDEs don't know where to find the module without proper configuration

## Solution
### Added Documentation
- **DEVELOPMENT_SETUP.md**: Comprehensive guide explaining the root cause and providing solutions for different platforms
- **README-DEV.md**: Quick start guide for developers

### Added Configuration Files
- **.vscode/settings.json**: VS Code configuration to resolve import errors
- **requirements-dev.txt**: Development dependencies list

### Platform Support
- Unix/Linux/macOS development setup instructions
- Windows development guidance using Docker/WSL
- IDE configuration for popular editors

## Testing
The solution has been verified to work on:
- Unix/Linux development environments
- macOS development environments
- Windows development environments using Docker or WSL

## Benefits
- Reduces onboarding friction for new contributors
- Provides clear solutions for development environment issues
- Improves developer experience by resolving import errors
- Offers platform-specific guidance

## Checklist
- [x] Added comprehensive documentation files
- [x] Added IDE configuration files
- [x] No breaking changes to existing functionality
- [x] No functional code changes
- [x] Files follow project conventions

## How to Test
1. Clone the repository
2. Set up development environment following DEVELOPMENT_SETUP.md
3. Configure IDE using provided configuration files
4. Verify import errors are resolved

For Windows users, we recommend using Docker or WSL as documented.

## Related Issues
This addresses common developer onboarding issues and helps reduce friction for new contributors to ERPNext.

Closes #XXXX (Import "frappe" could not be resolved basedpyright(reportMissingImports))