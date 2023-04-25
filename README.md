# GitHub Wiki Template

Repository template to manage a GitHub wiki that is synchronized with a GitHub project.\
This wiki is synchronized with the [project-repo-template](https://github.com/mhatzl/project-repo-template).

The structure is loosely related to the [arc42 documentation](https://docs.arc42.org/home/).\
To create system models, you should take a look at [C4](https://c4model.com/), and the related [Structurizr DSL](https://structurizr.com/).

This template is tailored to GitHub repositories, but the core concepts work for any project using a version control system.

## Wiki Pages

GitHub Wiki only considers files, and ignores any hierarchy set via folders.
This enforces that every filename is unique in the entire wiki.

This template is structured in a way to group related files, and enforce an order to first show more important pages on the wiki.

## Template Placeholders

In this template, many sections include placeholder text to provide some guidance of what the section should be about.
These placeholders are inside `{{ }}` blocks.

Some sections also include example content that is given inside `[[ ]]` blocks.

## GitHub Actions

This template contains the following GitHub actions:

- `auto-lock-prs` ... Used to lock PRs once they are closed
- `cla` ... Handles contributor license agreements with new contributors

# License

MIT Licensed
