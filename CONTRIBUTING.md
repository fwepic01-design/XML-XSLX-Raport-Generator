# Contributing to ExcelToWordConverter

First off, thank you for considering contributing to ExcelToWordConverter! It's people like you that make this tool better for everyone.


## How Can I Contribute?

There are many ways to contribute to ExcelToWordConverter, the most common being bug reports, feature requests, and pull requests.
You can also help by reviewing and commenting on existing issues and pull requests.
Contact me if you have any questions or idea.

### Reporting Bugs

This section guides you through submitting a bug report. Following these guidelines helps maintainers and the community understand your report, reproduce the behavior, and find related reports.

**Before Submitting A Bug Report**
- Check the issue tracker to see if the bug has already been reported.
- Check if the issue has been fixed — try to reproduce it using the latest `main` branch in the repository.

**How Do I Submit A (Good) Bug Report?**
- Use a clear and descriptive title for the issue to identify the problem.
- Describe the exact steps which reproduce the problem in as many details as possible.
- Provide specific examples to demonstrate the steps.
- Describe the behavior you observed after following the steps and point out what exactly is the problem with that behavior.
- Explain which behavior you expected to see instead and why.
- Include screenshots and animated GIFs if possible.
- If the problem is related to performance or memory, include a CPU profile capture with your report.

### Suggesting Enhancements

This section guides you through submitting an enhancement suggestion, including completely new features and minor improvements to existing functionality.

**Before Submitting An Enhancement Suggestion**
- Check the issue tracker to see if the enhancement has already been suggested.
- Check if the enhancement has already been implemented in the latest version.

**How Do I Submit A (Good) Enhancement Suggestion?**
- Use a clear and descriptive title for the issue to identify the suggestion.
- Provide a step-by-step description of the suggested enhancement in as many details as possible.
- Provide specific examples to demonstrate the steps.
- Describe the current behavior and explain which behavior you expected to see instead and why.
- Explain why this enhancement would be useful to most ExcelToWordConverter users.

### Pull Requests

The process described here has several goals:

- Maintain ExcelToWordConverter's quality
- Fix problems that are important to users
- Engage the community in working toward the best possible ExcelToWordConverter
- Enable a sustainable system for ExcelToWordConverter's maintainers to review contributions

Please follow these steps to have your contribution considered by the maintainers:

1. Follow all instructions in [the template](.github/PULL_REQUEST_TEMPLATE.md)
2. Follow the [styleguides](#styleguides)
3. After you submit your pull request, verify that all [status checks](https://help.github.com/articles/about-status-checks/) are passing

While the prerequisites above must be satisfied prior to having your pull request reviewed, the reviewer(s) may ask you to complete additional design work, tests, or other changes before your pull request can be ultimately accepted.

## Styleguides

### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line
- When only changing documentation, include `[ci skip]` in the commit title

### C# Styleguide

All C# code must adhere to [Microsoft's C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions).

- Use PascalCase for class names and method names
- Use camelCase for local variables and parameters
- Use readonly where appropriate
- Add XML documentation comments for public APIs
- Use regions to organize code within classes

### Documentation Styleguide

- Use [Markdown](https://daringfireball.net/projects/markdown) for documentation
- Reference methods and classes using backticks (`` `ClassName` ``)
- Follow the [Microsoft Style Guide](https://docs.microsoft.com/en-us/style-guide/welcome/) for terminology and formatting

## Additional Notes

### Issue and Pull Request Labels

This section lists the labels we use to help us track and manage issues and pull requests.

#### Type of Issue and Issue State

- `bug` - Issues that are bugs
- `enhancement` - Issues that are feature requests
- `documentation` - Issues that are documentation related
- `question` - Issues that are questions
- `help wanted` - Issues that need assistance
- `beginner` - Good for newcomers
- `duplicate` - Issues that are duplicates of other issues
- `invalid` - Issues that are invalid
- `wontfix` - Issues that won't be fixed

#### Pull Request Labels

- `work in progress` - Pull requests that are not ready for review
- `needs review` - Pull requests that need code review
- `needs testing` - Pull requests that need manual testing
- `ready to merge` - Pull requests that are ready to be merged
