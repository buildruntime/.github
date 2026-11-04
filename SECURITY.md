# Security policy

This policy applies to every repository under [buildruntime](https://github.com/buildruntime) that does not have its own `SECURITY.md`. If a repository has its own policy, follow that one.

## Reporting a vulnerability

**Do not report security vulnerabilities in public issues, pull requests or discussions.** Public reports put users at risk before a fix is available.

Report vulnerabilities privately through GitHub:

1. Go to the **Security** tab of the affected repository.
2. Choose **Report a vulnerability**. The form opens directly at `https://github.com/buildruntime/<repository>/security/advisories/new`, where `<repository>` is the name of the affected repository.
3. Fill in the form and submit it. Only you and the repository maintainers can see the report.

GitHub's documentation explains [how private vulnerability reporting works](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability).

If the repository does not show a **Report a vulnerability** button, open an issue in that repository titled "Private security contact requested". Do not include any details of the vulnerability, not even the affected component. A maintainer will reply with a private way to send the report.

## What to include

A report that can be reproduced is resolved much faster. Where you can, include:

- the affected repository, and the version, tag or commit you tested;
- the type of vulnerability, for example injection, path traversal or authentication bypass;
- the steps to reproduce it, with a minimal proof of concept if you have one;
- the impact: what an attacker can do, and what conditions they need;
- any known workaround or suggested fix;
- whether, and how, you would like to be credited.

## What happens next

After you submit a report, the maintainers will:

1. acknowledge it within five working days;
2. confirm whether it is a vulnerability, and tell you how severe we consider it, within fifteen working days of the acknowledgement;
3. work on a fix in a private fork linked to the advisory, and keep you informed of progress. You can comment on the draft advisory, and we may ask you to verify the fix;
4. release the fix, then publish a GitHub security advisory that describes the issue, the affected and fixed versions, and any workaround. Where appropriate, we request a CVE identifier through GitHub;
5. credit you in the advisory, unless you prefer not to be named.

If we decide the report is not a vulnerability, we will explain why. You are then free to discuss it in public, though we would ask you to tell us first.

## Disclosure

We follow coordinated disclosure. Please give us a reasonable chance to release a fix before you share details with anyone else. We aim to publish fixes within 90 days of the acknowledgement, and sooner for issues that are being actively exploited. If a fix will take longer, we will tell you why and agree a new date with you.

## Supported versions

Unless a repository's own policy says otherwise, security fixes are made on the default branch and included in the next release. Older releases do not receive fixes, so upgrade to the latest release to get them.

## Scope

In scope: the code, build configuration and published releases of repositories under [buildruntime](https://github.com/buildruntime).

Out of scope:

- vulnerabilities in third-party dependencies, which should be reported to the project concerned. Do tell us if a dependency is used in a way that makes a Buildruntime project exploitable;
- issues in GitHub itself, which should be reported through the [GitHub Bug Bounty program](https://bounty.github.com/);
- reports from automated scanners with no demonstrated impact;
- denial of service through volume of traffic;
- social engineering of maintainers or contributors.

## Good-faith research

We will not take legal action against, or ask anyone to take legal action against, people who research and report vulnerabilities in good faith under this policy. Good faith means that you:

- report the vulnerability privately and give us time to fix it;
- test only against your own installation or accounts;
- do not access, change or delete data that does not belong to you;
- do not degrade the service for other people.
