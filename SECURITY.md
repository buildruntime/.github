# Security policy

This policy applies to every repository under [buildruntime](https://github.com/buildruntime) that does not have its own `SECURITY.md`. If a repository has its own policy, follow that one.

## Keep vulnerability details private

**Never disclose details of a vulnerability in public.** That includes issues, pull requests, commits, discussions, comments, and anywhere outside GitHub, such as social media or blog posts. It also covers partial details: the affected component, the type of vulnerability, a proof of concept, or a link to one. Public details put users at risk before a fix is available.

The details stay private until a fix has been released and the security advisory is published, unless we agree a different arrangement with you.

## Reporting a vulnerability

Report vulnerabilities privately through GitHub:

1. Go to the **Security** tab of the affected repository.
2. Choose **Report a vulnerability**. The form is at `https://github.com/buildruntime/<repository>/security/advisories/new`, where `<repository>` is the name of the affected repository.
3. Fill in the form and submit it. Only you and the repository maintainers can see the report.

GitHub's documentation explains [how private vulnerability reporting works](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability).

### If there is no Report a vulnerability button

Private vulnerability reporting may not be turned on for every repository. If you cannot find the button, ask for a private security contact instead, and keep the details to yourself:

1. Open an issue in the affected repository, or in [buildruntime/.github](https://github.com/buildruntime/.github/issues/new/choose) if the repository does not accept issues.
2. Title it "Private security contact requested", and leave the body empty. Do not name the affected component or the type of vulnerability, in the issue or in later comments.
3. Wait for a maintainer to set up a private way to receive the report, such as turning on private vulnerability reporting for the repository. Send the details only through that private channel.

## What to include

A report that can be reproduced can be resolved sooner. Where you can, include:

- the affected repository, and the version, tag or commit you tested;
- the type of vulnerability, for example injection, path traversal or authentication bypass;
- the steps to reproduce it, with a minimal proof of concept if you have one;
- the impact: what an attacker can do, and what conditions they need;
- any known workaround or suggested fix;
- whether, and how, you would like to be credited.

## What happens next

Maintainers handle reports as their availability allows. How long each step takes depends on that and on the complexity of the issue, so we do not commit to fixed response times. We will keep you updated through the advisory. For each report, the maintainers will:

1. acknowledge it, and ask any questions needed to reproduce it;
2. confirm whether it is a vulnerability, and tell you how severe we consider it;
3. develop a fix in a temporary private fork linked to the advisory. You can comment on the draft advisory, and we may ask you to verify the fix;
4. release the fix, then publish a GitHub security advisory that describes the issue, the affected and fixed versions, and any workaround. Where appropriate, we request a CVE identifier through GitHub;
5. credit you in the advisory, unless you prefer not to be named.

If we conclude that the report is not a vulnerability, we will explain why in the private report. Please keep the details private even then. Ask us before you share them, because a second look sometimes changes the conclusion.

## Disclosure

We follow coordinated disclosure: a vulnerability is made public only once a fix is available and the advisory has been published. If a fix is taking longer than you think is reasonable, say so in the private report and we will discuss a disclosure date with you. Please do not disclose details before then.

## Supported versions

Unless a repository's own policy says otherwise, security fixes are made on the default branch and included in the next release. Older releases do not receive fixes, so upgrade to the latest release to get them.

## Scope

In scope: the code, build configuration and published releases of repositories under [buildruntime](https://github.com/buildruntime).

Out of scope:

- vulnerabilities in third-party dependencies, which should be reported to the project concerned. Do tell us, privately, if a dependency is used in a way that makes a Buildruntime project exploitable;
- issues in GitHub itself, which should be reported through the [GitHub Bug Bounty program](https://bounty.github.com/);
- reports from automated scanners with no demonstrated impact;
- denial of service through volume of traffic;
- social engineering of maintainers or contributors.

## Good-faith research

We will not take legal action against, or ask anyone to take legal action against, people who research and report vulnerabilities in good faith under this policy. Good faith means that you:

- report the vulnerability privately and keep the details private until it is disclosed;
- test only against your own installation or accounts;
- do not access, change or delete data that does not belong to you;
- do not degrade the service for other people.
