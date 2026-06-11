# Repository Guidelines

## Project Structure & Module Organization

This repository is a small GitHub Pages CV site.

- `index.md` contains the CV rendered by GitHub Pages and is the primary content file.
- `README.md` documents repository maintenance and publishing.
- `_config.yml` contains Jekyll/GitHub Pages configuration, currently the site theme.
- `AGENTS.md` documents contribution practices.

Keep CV content in `index.md` unless it requires site-wide configuration. If images or downloadable documents are added, place them in a clearly named directory such as `assets/images/` or `assets/documents/` and reference them with relative links.

## Build, Test, and Development Commands

There is no package manager, build script, or automated test suite. GitHub Pages renders the Markdown after changes are pushed.

- `git diff --check` detects whitespace errors.
- `git diff -- index.md _config.yml` reviews content and configuration changes.
- `git status --short` confirms which files will be included in a commit.

For content changes, use a Markdown preview in your editor and verify headings, lists, and links before opening a pull request. If a local Jekyll environment is already installed, `bundle exec jekyll serve` may be used, but this repository does not currently provide a `Gemfile`.

## Coding Style & Naming Conventions

Use standard Markdown with ATX headings (`#`, `##`, `###`) and hyphenated unordered lists. Keep one blank line around headings and lists, remove trailing whitespace, and use descriptive link text rather than raw URLs. Preserve the existing section hierarchy: one document title, second-level CV sections, and third-level entries.

Use lowercase YAML keys and two-space indentation in `_config.yml`. Name new asset files descriptively with lowercase kebab-case, for example `assets/documents/clint-pijuan-cv.pdf`.

## Testing Guidelines

Validation is primarily editorial and visual. Check spelling, dates, contact details, link targets, and rendered Markdown. Confirm `_config.yml` remains valid YAML and run `git diff --check`. For layout or theme changes, inspect the deployed GitHub Pages site on desktop and mobile widths.

## Commit & Pull Request Guidelines

Recent history uses short, imperative, sentence-style subjects such as `Update README.md` and `Set theme jekyll-theme-cayman`. Prefer a more specific subject when possible, for example `Update software development experience`.

Pull requests should explain the content changed and why. Include the affected sections, note any new assets or configuration changes, and attach a screenshot when rendering or theme behavior changes.
