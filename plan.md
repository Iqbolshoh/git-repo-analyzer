# Development Plan — Git Repo Analyzer

This document is the project's working plan and progress tracker. Update it as tasks are completed, decisions change, or scope is revised.

## Project Objective

Build a lightweight, safe, cross-platform CLI that analyzes a Git repository and produces a clear, actionable repository health report.

## Working Rules

- [ ] Keep this plan current; check off only work that is actually completed.
- [ ] Add notable decisions and scope changes to the **Decision Log**.
- [ ] Record completed work in the **Progress Log**.
- [ ] Do not mark a task complete until it is implemented and, where relevant, tested.
- [ ] Keep the tool read-only by default. No target-repository modifications without explicit future opt-in.
- [ ] Prefer small, focused commits.

## Phase 0 — Project Setup

- [ ] Choose implementation language and CLI framework
- [ ] Define supported operating systems and minimum runtime versions
- [ ] Set up project structure
- [ ] Add package/dependency configuration
- [ ] Configure formatting and linting
- [ ] Configure test framework
- [ ] Add CI workflow
- [ ] Add initial license
- [ ] Add contribution and security guidance (as scope warrants)

## Phase 1 — CLI Foundation

- [ ] Implement CLI entry point
- [ ] Add help and version output
- [ ] Accept a target repository path (default: current directory)
- [ ] Validate that the target path exists
- [ ] Validate that the path is a Git repository
- [ ] Handle Git-not-installed and Git-command-failure cases gracefully
- [ ] Establish consistent output formatting
- [ ] Add tests for CLI and error cases

## Phase 2 — Repository Overview

- [ ] Detect repository root
- [ ] Identify current branch
- [ ] Report working-tree status
- [ ] Count local branches
- [ ] Count commits (document the exact counting method)
- [ ] Report repository metadata available through Git
- [ ] Add unit/integration tests

## Phase 3 — Commit History Analysis

- [ ] Show recent commit list
- [ ] Show commit hash (short form)
- [ ] Show subject
- [ ] Show author and date
- [ ] Provide activity summary for a configurable/default period
- [ ] Handle repositories with no commits
- [ ] Add tests for history output and edge cases

## Phase 4 — Branch Analysis

- [ ] List local branches
- [ ] Mark the current branch
- [ ] Show upstream/tracking branch if available
- [ ] Detect branches with no upstream (report only; don't assume they're stale)
- [ ] Add tests

## Phase 5 — Large File Detection

- [ ] Scan tracked files
- [ ] Report file sizes
- [ ] Define default large-file threshold
- [ ] Allow threshold customization
- [ ] Exclude Git internals from scanning
- [ ] Handle missing files and unusual paths safely
- [ ] Add tests

## Phase 6 — `.gitignore` Checks

- [ ] Check for `.gitignore`
- [ ] Check common ignore-rule omissions (tailor checks to detected ecosystem when possible)
- [ ] Avoid false positives and explain each warning
- [ ] Do not edit `.gitignore` automatically
- [ ] Add tests

## Phase 7 — Health Report

- [ ] Define report sections and severity levels
- [ ] Aggregate findings from completed analyzers
- [ ] Provide concise summary and actionable recommendations
- [ ] Avoid arbitrary/unexplained health scores
- [ ] Add terminal report
- [ ] Add tests for report aggregation

## Phase 8 — User Experience

- [ ] Add sensible defaults
- [ ] Improve terminal readability
- [ ] Add quiet/verbose modes if justified
- [ ] Add output format options (e.g., JSON) if justified
- [ ] Add clear exit codes
- [ ] Review error messages and edge cases

## Phase 9 — Quality and Release

- [ ] Review test coverage
- [ ] Run full test suite
- [ ] Check lint/format
- [ ] Review security and dependency footprint
- [ ] Test on supported operating systems
- [ ] Finalize README usage and installation instructions
- [ ] Create release notes
- [ ] Tag first release (versioning scheme to be decided)

## Current Status

**Status:** Planning

**Current phase:** Phase 0 — Project Setup

**Last updated:** YYYY-MM-DD

## Progress Log

Use newest entries at the top. Record what was actually done, results, and any follow-up tasks.

### YYYY-MM-DD
- Started project planning.
- Created initial README and roadmap.
- Next: select stack and initialize project structure.

## Decision Log

Record important choices and the reason behind them. Newest entries at the top.

| Date | Decision | Reason / context |
|---|---|---|
| YYYY-MM-DD | Read-only analysis by default | Avoid accidentally modifying user repositories. |
| YYYY-MM-DD | Health report should explain findings, not use an opaque score | Make results transparent and actionable. |

## Change Log

Track meaningful project changes (not every tiny edit).

| Date | Change | Notes |
|---|---|---|
| YYYY-MM-DD | Project planning initiated | Initial scope, roadmap, and tracking structure established. |

## Notes / Ideas

- Keep future ideas here until they are accepted into the roadmap.
- Distinguish planned features from implemented features.
- Update README feature status when implementation changes.
