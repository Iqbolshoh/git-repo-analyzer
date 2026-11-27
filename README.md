# Git Repo Analyzer

A lightweight CLI tool for analyzing Git repositories and generating useful repository health insights.

`git-repo-analyzer` helps developers quickly understand a repository's structure, activity, and hygiene through a simple command-line interface.

## Features

> Planned features for the initial development roadmap. Features will be marked as implemented as they are completed.

- [ ] Repository overview and statistics
- [ ] Commit history analysis
- [ ] Branch overview
- [ ] Identify large files
- [ ] `.gitignore` checks
- [ ] Repository health summary
- [ ] Clear, readable terminal output
- [ ] Support for analyzing a repository path

## Goals

- Provide a fast, simple repository overview from the terminal.
- Surface potential repository hygiene issues.
- Make reports understandable and actionable.
- Keep the tool lightweight and easy to install and use.
- Build a maintainable, testable codebase.

## Usage

Usage examples will be added once the first CLI version is implemented.

```bash
# Planned example
git-repo-analyzer .
```

## Analysis Areas

### 1. Repository statistics
- Repository path and detected status
- Number of branches
- Commit count
- Repository size (where practical)

### 2. Commit history
- Recent commits
- Commit frequency and activity overview
- Author summary, where available

### 3. Branch analysis
- List local branches
- Identify the current branch
- Show branch tracking information when available

### 4. Large files
- Find large tracked files
- Show file size and path
- Use configurable thresholds in a future version

### 5. `.gitignore` hygiene
- Check whether `.gitignore` exists
- Identify common files/directories that may be missing ignore rules
- Avoid making automatic changes without explicit user confirmation

### 6. Repository health summary
- Summarize findings
- Highlight warnings and potential improvements
- Provide an overall, transparent report (not an unexplained score)

## Principles

- **Read-only by default:** analysis should not modify the target repository.
- **Safe:** never delete files, rewrite Git history, or change repository configuration automatically.
- **Transparent:** explain why a finding is reported.
- **Portable:** aim to work across common operating systems.
- **Useful output:** prioritize actionable insights over noisy checks.

## Project Status

Early development. The feature checklist and usage documentation will be updated as implementation progresses.

See [`plan.md`](plan.md) for the development roadmap and progress log.

## Contributing

Contributions, bug reports, and feature suggestions are welcome. Please open an issue before making a large change so the scope can be discussed.

## License

License has not been selected yet. A license will be added before the project is considered ready for public use.
