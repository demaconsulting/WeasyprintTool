# Agent Instructions

This document contains instructions for AI agents working on the WeasyprintTool project.

## Overview

WeasyprintTool is a repackaging of [Weasyprint][weasyprint-url] as a [.NET tool][dotnet-tools-url]. The project uses GitHub Actions for building and releasing the NuGet package.

## Project Structure

- `/pack/` - NuGet package configuration and build files
  - `DemaConsulting.WeasyprintTool.csproj` - Project file
  - `DemaConsulting.WeasyprintTool.nuspec` - NuGet package specification
  - `/tools/` - .NET tool binaries (populated during build)
  - `/win-x64/` - Windows x64 Weasyprint binaries (populated during build)
- `/.github/` - GitHub Actions workflows and templates
  - `/workflows/` - CI/CD workflows
  - `/ISSUE_TEMPLATE/` - Issue templates for bugs and features
- Configuration files:
  - `.cspell.json` - Spelling check configuration
  - `.markdownlint.json` - Markdown linting configuration
  - `.gitignore` - Git ignore patterns

## Important Rules

### README.md Requirements

**CRITICAL**: The `README.md` file is distributed in the NuGet package. It has special requirements:

- **All links MUST be absolute URLs** (e.g., `https://github.com/demaconsulting/WeasyprintTool/...`)
- **NEVER use relative links** (e.g., `./CONTRIBUTING.md`, `#section`)
- This ensures links work correctly when README.md is viewed in the NuGet package
- Always verify links in README.md are absolute before committing

### Markdown Link Format

All Markdown files should use the reference link format:

```markdown
[link text][reference-id]

[reference-id]: https://example.com
```

Benefits:

- Easier to maintain links
- More readable text
- Consistent style across documentation

### Quality Checks

Before completing any task, always run these quality checks:

1. **Spelling**: `npx cspell "**/*.md"`
   - Checks spelling in all Markdown files
   - Add project-specific words to `.cspell.json` if needed
   - Never commit files with spelling errors

2. **Markdown Linting**: `npx markdownlint-cli "**/*.md"`
   - Checks Markdown formatting
   - Ensures consistent style
   - Fix all warnings before committing

3. **Build Verification**: Check that workflows pass
   - Quality Checks job should pass
   - Build job should pass

### Testing Changes

When making changes:

1. Run spelling check: `npx cspell "**/*.md"`
2. Run markdown lint: `npx markdownlint-cli "**/*.md"`
3. Fix any issues found
4. Verify changes work as expected
5. Commit only after all checks pass

## Build Process

The project uses GitHub Actions workflows:

1. **build-on-push.yaml** - Triggers on every push
   - Runs quality checks (spelling, markdown linting)
   - Calls build.yaml workflow
2. **build.yaml** - Reusable build workflow
   - Downloads DotnetToolWrapper
   - Downloads Weasyprint binaries
   - Generates SBOM (Software Bill of Materials)
   - Creates NuGet package
3. **release.yaml** - Handles releases
   - Creates releases with proper versioning

## Dependencies

### External Dependencies

- [DotnetToolWrapper][wrapper-url] - .NET tool wrapper framework
- [Weasyprint][weasyprint-url] - Document factory (Python-based)

### Dependency Updates

Dependabot is configured to automatically:

- Update GitHub Actions weekly
- Update NuGet packages weekly
- Group updates to reduce PR count

## Code Style

- Follow existing patterns in the codebase
- Keep changes minimal and focused
- Write clear commit messages
- Update documentation when needed

## Documentation

When updating documentation:

- Use Markdown reference links
- Check spelling with cspell
- Lint with markdownlint
- Ensure README.md uses absolute URLs only
- Keep documentation concise and clear

## Common Tasks

### Adding a Word to Spell Check

Edit `.cspell.json` and add to the `words` array:

```json
{
  "words": [
    "newword"
  ]
}
```

### Updating Weasyprint Version

Edit `.github/workflows/build-on-push.yaml` and `.github/workflows/release.yaml` to update the `weasyprint` version input.

### Adding Issue Templates

Add new templates to `.github/ISSUE_TEMPLATE/` following the existing format.

## Quality Standards

All changes must:

1. Pass spelling checks (`cspell`)
2. Pass markdown linting (`markdownlint`)
3. Follow documentation standards
4. Use absolute URLs in README.md
5. Use reference-style links in Markdown
6. Include appropriate tests/validation

## Resources

- [Weasyprint Documentation][weasyprint-docs-url]
- [.NET Tools Documentation][dotnet-tools-url]
- [GitHub Actions Documentation][github-actions-url]

[weasyprint-url]: https://weasyprint.org/
[weasyprint-docs-url]: https://doc.courtbouillon.org/weasyprint/stable/
[dotnet-tools-url]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools
[wrapper-url]: https://github.com/demaconsulting/DotnetToolWrapper
[github-actions-url]: https://docs.github.com/en/actions
