# The Debugging Challenge: A Broken System

That is what the documentation says the project does. However, when you arrived for your first day as the new maintainer, you discovered the repository was left in a state of absolute chaos by your predecessor.

The system is plagued by silent ailments and hidden traps. Your mission is to step into the unknown, uncover the root causes of the repository's decay, and restore the Mobius project to its former glory.

Critical Directive: You must only modify the files necessary to fix the specific bugs outlined below. Do not alter unrequired files, rewrite unrelated logic, or change the intended architecture of the system.

Good luck. The project is counting on you.

# Mobius

Mobius is a compact static documentation site generator for Markdown-based
projects.

## Installation

```bash
python -m venv .venv
source .venv/bin/activate
pip install -e .
```

## What it does

- converts Markdown content into a static HTML site
- reads YAML front matter for page metadata
- renders pages with Jinja2 themes
- loads small plugins from the local `plugins/` directory
- rebuilds content while files change

## Layout

- `content/` contains source Markdown files
- `themes/default/` provides the built-in templates
- `plugins/` holds local extensions
- `expected_site/` stores the reference HTML output

## Documentation

- [Installation](INSTALLATION.md)
- [Contributing](CONTRIBUTING.md)
- [Project overview](PROJECT_OVERVIEW.md)
- [Maintainer flow](MAINTAINER_FLOW.md)

## Usage

```bash
mobius build
mobius serve --watch
```

The default build writes to `site/`.
