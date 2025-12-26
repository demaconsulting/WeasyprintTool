# Contributing to WeasyprintTool

Thank you for your interest in contributing to WeasyprintTool! This document provides guidelines and instructions for contributing to this project.

## Code of Conduct

This project adheres to a Code of Conduct. By participating, you are expected to uphold this code. Please read [CODE_OF_CONDUCT.md][code-of-conduct-url] before contributing.

## How to Contribute

### Reporting Bugs

If you find a bug, please report it by:

1. Checking if the issue already exists in [GitHub Issues][issues-url]
2. If not, create a new issue using the bug report template
3. Provide as much detail as possible including:
   - Version of WeasyprintTool
   - .NET version
   - Operating system
   - Steps to reproduce
   - Expected vs actual behavior

### Suggesting Features

We welcome feature suggestions! To suggest a feature:

1. Check if the feature has already been requested in [GitHub Issues][issues-url]
2. If not, create a new issue using the feature request template
3. Describe the problem you're trying to solve
4. Explain your proposed solution
5. Consider any alternatives you've thought about

### Contributing Code

1. **Fork the repository** on GitHub
2. **Clone your fork** locally
3. **Create a branch** for your changes
4. **Make your changes** following our coding standards
5. **Test your changes** thoroughly
6. **Commit your changes** with clear commit messages
7. **Push to your fork** and submit a pull request

## Development Guidelines

### Project Structure

- `/pack/` - NuGet package configuration and build files
- `/.github/` - GitHub Actions workflows and templates
- `README.md` - Project documentation (distributed in NuGet package)

### Coding Standards

- Follow existing code style and conventions
- Write clear, self-documenting code
- Add comments only when necessary to explain complex logic

### Documentation Standards

#### README.md Special Requirements

The `README.md` file is distributed in the NuGet package and has special requirements:

- **All links MUST use absolute URLs** (e.g., `https://github.com/...`)
- **Do NOT use relative links** (e.g., `./CONTRIBUTING.md`)
- This ensures links work correctly when the README is viewed in the NuGet package

#### Markdown Link Format

All Markdown files should use the reference link format:

```markdown
[link text][reference-id]

[reference-id]: https://example.com
```

This makes links easier to maintain and read.

### Quality Checks

Before submitting a pull request:

1. **Spelling**: Run `npx cspell "**/*.md"` to check spelling
2. **Markdown Linting**: Run `npx markdownlint-cli "**/*.md"` to check formatting
3. **Build**: Ensure the project builds successfully
4. **Testing**: Test your changes thoroughly

The CI pipeline will automatically run these checks on your pull request.

### Commit Messages

- Use clear, descriptive commit messages
- Start with a verb in present tense (e.g., "Add feature", "Fix bug")
- Keep the first line under 72 characters
- Add details in the body if needed

## Building the Project

WeasyprintTool uses GitHub Actions for building. The build process:

1. Downloads the DotnetToolWrapper
2. Downloads Weasyprint binaries
3. Creates the NuGet package

To test the build locally, you can examine the workflow files in `.github/workflows/`.

## Testing

- Test your changes with different .NET versions (8.0, 9.0, 10.0)
- Test on different operating systems when possible
- Verify the tool works correctly with various Weasyprint commands

## Pull Request Process

1. Update documentation if needed
2. Ensure all quality checks pass (spelling, markdown linting)
3. Update the README.md if you're changing functionality
4. Your pull request will be reviewed by maintainers
5. Address any feedback from reviewers
6. Once approved, your changes will be merged

## Questions?

If you have questions about contributing:

- Check existing [GitHub Issues][issues-url]
- Start a [GitHub Discussion][discussions-url]
- Review the [README.md][readme-url]

## License

By contributing to WeasyprintTool, you agree that your contributions will be licensed under the BSD-3-Clause License.

[code-of-conduct-url]: https://github.com/demaconsulting/WeasyprintTool/blob/main/CODE_OF_CONDUCT.md
[issues-url]: https://github.com/demaconsulting/WeasyprintTool/issues
[discussions-url]: https://github.com/demaconsulting/WeasyprintTool/discussions
[readme-url]: https://github.com/demaconsulting/WeasyprintTool/blob/main/README.md
