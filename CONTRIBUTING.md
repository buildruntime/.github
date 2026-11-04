# Contributing

Thank you for taking the time to improve a Buildruntime project. This guide applies to every repository under [buildruntime](https://github.com/buildruntime) that does not have its own `CONTRIBUTING.md`. Project-specific instructions, such as how to install dependencies or run the tests, are in each repository's README and take precedence over this guide where the two differ.

Everyone taking part is expected to follow the [Code of Conduct](https://github.com/buildruntime/.github/blob/main/CODE_OF_CONDUCT.md).

## Before you start

- **Security issues** are never reported in public. Follow the [security policy](https://github.com/buildruntime/.github/blob/main/SECURITY.md) instead.
- **Search first.** Check open and closed issues and pull requests to see whether the problem is already known or the change has already been discussed.
- **Discuss larger changes before writing them.** For a new feature, a change in behaviour, a new dependency or a refactor that touches many files, open an issue first and describe the problem you want to solve. Agreeing on the approach early saves you from writing code that cannot be merged.
- **Small fixes can go straight to a pull request.** Typos, broken links, clear bug fixes with a test, and documentation corrections do not need an issue first.
- **Say that you are working on something.** Comment on the issue so that two people do not solve the same problem in parallel. If you stop working on it, say so too.

## Workflow

1. Fork the repository and clone your fork.
2. Add the original repository as a remote, so you can keep your fork up to date. Replace `<repository>` with the name of the repository you forked:

   ```bash
   git remote add upstream https://github.com/buildruntime/<repository>.git
   git fetch upstream
   ```

3. Create a branch from the latest default branch of the original repository (see [Branches](#branches)).
4. Make your change, with tests and documentation (see [What a change includes](#what-a-change-includes)).
5. Run the project's tests, linters and formatters locally. The README lists the commands.
6. Push the branch to your fork and open a pull request against the default branch of the original repository.
7. Respond to review until the pull request is approved and merged (see [Review](#review)).

## Branches

Create one branch per change and keep it focused on a single topic. Name it after the kind of change and what it does, in lowercase words separated by hyphens:

```text
<type>/<short-description>
```

| Type | Use for |
| :-- | :-- |
| `fix` | A bug fix. |
| `feature` | New behaviour or a new capability. |
| `docs` | Documentation only. |
| `refactor` | A change in structure that keeps behaviour the same. |
| `test` | New or improved tests, with no change to the code under test. |
| `chore` | Build, tooling, dependency or CI changes. |

For example: `fix/timeout-on-empty-response`, `docs/configuration-examples`.

Before you ask for review, bring your branch up to date with the default branch:

```bash
git fetch upstream
git rebase upstream/main
```

Use the repository's actual default branch name if it is not `main`. Rebasing your own branch and force-pushing it to your fork is fine (`git push --force-with-lease`). Never rewrite a branch that someone else is working on.

## Commits

Write commits that a reviewer can read one at a time and that someone running `git log` in a year can still understand.

- Write the subject line in the imperative mood and sentence case, as if completing the sentence "This commit will…": `Handle empty responses in the HTTP client`, not `handled empty responses` or `Fixes`.
- Keep the subject to 72 characters or fewer, with no full stop at the end.
- If the change needs explaining, leave a blank line after the subject and write a body, wrapped at 72 characters. Explain what changed and why. The diff already shows how.
- Make each commit one logical change that builds and passes the tests. Keep formatting changes, renames and behaviour changes in separate commits.
- Squash "fix typo" and "address review" commits into the commit they correct before the pull request is merged, or leave them for the maintainer to squash on merge.
- Never commit secrets, credentials, personal data, or build output that the project does not already track.

An example:

```text
Retry idempotent requests after a connection reset

Requests that fail with ECONNRESET before any response bytes arrive
are now retried up to the configured limit. Non-idempotent methods
are still not retried, because the server may already have acted on
them.

Fixes #42
```

## What a change includes

A pull request is ready for review when it contains everything needed to merge it:

- **Tests.** Bug fixes include a test that fails without the fix. New behaviour includes tests that cover it, including the error cases.
- **Documentation.** Update the README, reference documentation and code comments that describe the behaviour you changed. If users have to do something differently, say what.
- **Changelog.** If the repository keeps a changelog, add an entry for any change that users will notice.
- **No unrelated changes.** Leave reformatting, dependency upgrades and drive-by refactoring for separate pull requests. They make review slower and the history harder to follow.
- **Compatibility.** Call out anything that breaks existing users, such as a changed default, a removed option or a new minimum runtime version, and explain why it is necessary.

## Pull requests

- Fill in the pull request template. Explain the problem, the approach you chose, and how you tested it. Link the issue it resolves with a closing keyword, for example `Fixes #123`.
- Keep pull requests small. Several focused pull requests are reviewed faster and more thoroughly than one large one. If a change is large by nature, say how you suggest reviewing it.
- Open a draft pull request if you want early feedback on an approach before it is finished.
- Make sure the automated checks pass. If a check fails for a reason unrelated to your change, say so in the pull request instead of working around it.
- Do not disable, skip or delete tests to make a pull request pass.

## Review

Every pull request is reviewed by a maintainer before it is merged. Reviewers look at, in roughly this order:

1. **Correctness.** Does it do what it says, including the edge cases and failure paths?
2. **Tests.** Would the tests catch a regression?
3. **Design.** Does it fit the existing structure, and is it as simple as the problem allows?
4. **Readability.** Will the next person understand it without the pull request open beside it?
5. **Documentation and compatibility.** Is the change documented, and is any breaking change necessary and called out?

What you can expect from maintainers:

- A first response to a new pull request within five working days. A first response may be a question or a request for changes rather than a full review.
- Comments that explain the reasoning behind a request, and that make clear which requests must be addressed and which are suggestions.
- A clear decision. If a change does not fit the project, we will say so and explain why, rather than leaving the pull request open indefinitely.

What we ask of contributors:

- Reply to each review comment, even if only to say it is done. Push changes as new commits during review, so the reviewer can see what changed since their last pass.
- Leave the conversation open for the reviewer to resolve, unless the change is trivial.
- If you disagree with a request, say so and explain why. Review is a discussion, not a list of orders.
- If you cannot continue, say so. A maintainer may finish the work, with credit to you. A pull request with no reply to requested changes for 30 days may be closed, and can be reopened at any time.

Maintainers merge approved pull requests, usually by squashing them into a single commit on the default branch. The pull request title becomes the commit subject, so write it the same way as a commit subject.

## Reporting bugs and requesting features

Open an issue in the repository concerned, and choose the form for a [bug report](https://github.com/buildruntime/.github/blob/main/.github/ISSUE_TEMPLATE/bug_report.yml) or a [feature request](https://github.com/buildruntime/.github/blob/main/.github/ISSUE_TEMPLATE/feature_request.yml). [`SUPPORT.md`](https://github.com/buildruntime/.github/blob/main/SUPPORT.md) explains where everything else goes.

## Licensing of contributions

By contributing, you agree that your contribution is licensed under the licence of the repository you contribute to, as stated in its `LICENSE` file. You must have the right to submit the work, and if it includes code or text from elsewhere, its licence must be compatible with the project's and its origin must be stated in the pull request. There is no separate contributor licence agreement.
