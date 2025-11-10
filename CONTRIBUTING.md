# Contributing to Skedulo Plus Examples

Thank you for your interest in contributing to the Skedulo Plus Examples repository! We welcome contributions from the community to help improve and expand our examples.

## Getting Started

1. Ensure you read the general [CONTRIBUTING](https://github.com/skeduloDevelopers/.github/blob/main/profile/CONTRIBUTING.md) and [CODE OF CONDUCT](https://github.com/skeduloDevelopers/.github/blob/main/profile/CODE_OF_CONDUCT.md) instructions.
2. Familiarize yourself with the codebase and review the [README](README.md) for details on the available examples and how to deploy them.
3. Check the existing issues or create a new issue before starting work on a significant contribution. This helps us coordinate efforts and provide guidance.
4. Fork this repository.
5. Set up your development environment following the instructions on the [Skedulo docs site](https://docs.skedulo.com/developer-guides/customize-and-extend-mobile/skedulo-plus-extensions/getting-started/getting-started-mex/)
6. Create a _topic_ branch in your fork based on the **main** branch.
7. Make your changes in your fork.
8. Submit a pull request when you're ready. We'll review your code, suggest any needed changes, and merge it in.

## Types of Contributions

We welcome various types of contributions, including:

- **New Mobile Extension examples**: Create new examples that demonstrate different use cases or components
- **Improvements to existing examples**: Enhance documentation, add features, or improve code quality
- **Bug fixes**: Identify and fix issues in the example extensions
- **Documentation updates**: Improve README files, add comments, or create tutorials

## Mobile Extension Guidelines

When contributing Mobile Extensions, please ensure:

- Your extension follows the folder structure convention used in this repository
- Include all required files: `metadata.json`, `ui_def.json`, `staticFetch.json`, `instanceFetch.json`, and `upload_config.json`
- Provide clear documentation in both the folder-level README and the main repository README, including screenshots
- Test your extension thoroughly
- Use meaningful names for your extension that clearly indicate its purpose

## Branches

- We work in **main**.
- Our released (aka. _production_) branch is **main**.
- Development happens in _topic_ branches (feature and/or bug-fix).
    - Feature and bug-fix branches are based on **main**
    - Branches _should_ be kept up-to-date using `rebase`
    - See below for further merge instructions

### Branch Naming Convention

When creating _topic_ branches in this repository, please prefix with `<developer-name>/` to keep the repository organized.

Examples:
- `sophiew/add-contact-form-example`
- `johnd/fix-product-validation`
- `mariaf/improve-documentation`

### Merging Between Branches

- We try to limit merge commits as much as possible.
- _Topic_ branches are:
    1. Based on **main** and will be
    1. Squash-merged into **main**

## Pull Requests

- Develop features and bug fixes in _topic_ branches.
- _Topic_ branches can live in forks (external contributors) or within this repository (committers with write access).
- Provide a clear description of the changes in your pull request.
- Reference any related issues using the `#issue-number` syntax.
- Ensure your code follows the existing style and conventions.
- Update documentation as needed.

### Pull Request Checklist

Before submitting a pull request, please ensure:

- [ ] Your Mobile Extension deploys successfully using the Skedulo CLI
- [ ] All JSON files are properly formatted
- [ ] Documentation has been updated (README.md and any relevant in-folder documentation, including screenshots)
- [ ] You've tested the extension in a Skedulo environment
- [ ] Your branch is up to date with **main**
- [ ] Your commit messages are clear and descriptive

### Merging Pull Requests

- Pull request merging is restricted to squash & merge only.
- This keeps our commit history clean and makes it easier to track changes.

## Questions or Need Help?

If you have questions or need assistance:

- Review the [Mobile Extension documentation](https://docs.skedulo.com/developer-guides/customize-and-extend-mobile/skedulo-plus-extensions/mex-intro/)
- Check existing issues for similar questions
- Create a new issue with the `question` label
- Contact your Customer Success Manager

## Recognition

Contributors who make significant contributions will be recognized in the repository. We appreciate your time and effort in making these examples better for the entire Skedulo developer community!
