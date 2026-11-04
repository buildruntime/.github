<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/buildruntime/buildruntime/main/assets/brand/logo-horizontal-dark.svg">
  <img alt="Buildruntime" src="https://raw.githubusercontent.com/buildruntime/buildruntime/main/assets/brand/logo-horizontal-light.svg" height="24">
</picture>

# Community health files

Default community health files for repositories owned by [buildruntime](https://github.com/buildruntime). GitHub uses a file from this repository whenever a Buildruntime repository does not have its own file of the same type.

## Contents

| File | Purpose |
| :-- | :-- |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to propose changes: workflow, branches, commits, pull requests and review. |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Contributor Covenant 2.1 and how to report a concern. |
| [`SECURITY.md`](SECURITY.md) | How to report a vulnerability privately and what happens next. |
| [`SUPPORT.md`](SUPPORT.md) | Where to report bugs, request features and ask questions. |
| [`PULL_REQUEST_TEMPLATE.md`](PULL_REQUEST_TEMPLATE.md) | Description and checklist added to every new pull request. |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | Bug report and feature request forms, and the issue chooser configuration. |
| [`LICENSE`](LICENSE) | CC BY 4.0, covering the documentation in this repository. |

## How the defaults apply

- For each file type, GitHub looks in the repository's `.github` folder, then its root, then its `docs` folder. If none of them has the file, GitHub uses the one here.
- Issue templates are all or nothing. A repository with valid templates or a `config.yml` in its own `.github/ISSUE_TEMPLATE` folder uses only those, and none of the forms here.
- The issue forms apply the `bug` and `enhancement` labels. A label is only applied if it exists in the repository where the issue is opened. Both are part of GitHub's default label set.
- Licences are not inherited. Every repository needs its own `LICENSE` file, chosen for what it contains.

## Overriding a file

Add a file with the same name to the repository that needs something different, in its `.github` folder, root or `docs` folder. A common case is a project-specific `SECURITY.md` that lists supported versions. Start from the version here and change only what differs, so the projects stay consistent.

## Changing the defaults

A change here applies to every Buildruntime repository that has no file of its own, so it needs the same care as a change to a shared library. Open a pull request that explains the reason for the change, and follow [`CONTRIBUTING.md`](CONTRIBUTING.md). Links in these files are absolute, because GitHub shows them in the context of other repositories, where relative links would not resolve.

## Contact

Email [manav.it3101@gmail.com](mailto:manav.it3101@gmail.com) about anything that should not be raised in a public issue, including conduct concerns. Report security vulnerabilities through GitHub's private vulnerability reporting, as described in [`SECURITY.md`](SECURITY.md). Questions, bug reports and feature requests belong in the issues of the repository concerned. [`SUPPORT.md`](SUPPORT.md) has the details.

## Licence

The documentation in this repository is licensed under the [Creative Commons Attribution 4.0 International License](LICENSE) (CC BY 4.0). [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) is adapted from the [Contributor Covenant](https://www.contributor-covenant.org), version 2.1, which is published under the same licence.
