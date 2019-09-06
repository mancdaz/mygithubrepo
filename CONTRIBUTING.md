# Contributing to this repository

# Audience
This set of contributing guidelines is for both external contributors, as well as Verne Global employees. There are number of references to using JIRA issue number in this document. If you are an external contributor and do not have access to the Verne Global JIRA instance, please ignore these references.

# Table of Contents
1. [Commits and pull requests](#commits-release-notes-pull-requests)
    1. [Fixing a bug](#fixing-a-bug)
    2. [Commits](#commits)
    3. [Pull requests](#pull-requests)
        1. [Reviewing pull requests](#reviewing-pull-requests)
        2. [Merging pull requests](#merging-pull-requests)

## Commits and pull requests
### Fixing a bug

1. Clone the repo, and commit changes to a new branch, named using the convention <JIRA-ISSUE-NUMBER>-description-of-change. e.g. ```HPCDIR-9999-add-contributing```
2. Make pull requests against the master branch in the repo.
3. Reference the JIRA issue in both the commit message and the pull request message.

### Commits

Please avoid the following in a commit:

* Mixing whitespace changes with functional code changes.
* Mixing two unrelated functional changes in the same commit.
* Sending large new features in a single commit.

Expected git commit message structure (Based on [this article](https://chris.beams.io/posts/git-commit/)):

* The first line should ideally be limited to 50 characters, but must be no more than 70 characters.
* The first line should include the JIRA ticket number, followed by a brief description of the change. e.g. ```HPCDIR-9999:Remove a typo in README.md```
* The first line should not end with a full stop and the first word of the description should be capitalised.
* Use the imperative mood in the subject line - e.g. ```Fix a typo in CONTRIBUTING.md```, ```Remove if/else block in myfile.sh```, ```Eat your dinner```.
* Insert a single blank line after the first line, if making a multi-line commit.
* Subsequent lines should be wrapped at 72 characters.
* Provide a detailed description of the change in the following lines, using the guidelines in the section below.

In your commit message please consider the following points:

* The commit message must be descriptive and contain all the information required to fully understand and review the patch.
* Do not assume the reviewer understands what the original problem was.
* Do not assume the reviewer has access to external web services or site.
* Do not assume the code is self-evident or self-documenting.
* Describe why the change is being made.
* Ensure sufficient information is provided to review your commit.
* Each commit should ideally solve a single problem. Where there are several things to fix to reach the goal identified by the card, multiple commits should be used. Each commit should be as easy as possible to consume (or revert) as a single, complete change.

### Pull requests

* Pull Requests (PRs) should be made from a development branch in the main repo. 
* A PR should contain a single commit, or multiple commits all related to the problem being solved by the PR.
* The PR title and message should contain information relevant to why the commit(s) are happening. This can be based off the commit message.
* As with commit messages, the PR description should reference the original issue.

#### Reviewing pull requests

When reviewing a PR, please ensure the included commit(s):

* Actually works to fix the issue.
* Passes any tests that are configured to run.
* Contains a single commit, or multiple commits all related to the problem being solved by the PR.
* Does not overreach. Each PR should be self contained to only address the issue at hand (see above).

#### Merging pull requests

In order for a PR to be merged, the following criteria should be met:

* Any configured tests must have passed.
* There must be at least 1 member of the engineering team review and give the PR a +1 approval using the review guidelines above. Protected branches are used to prevent un-reviewed code from being merged.
* Use the gitlab/github code review function so that your comments are collated into a single review, and use the 'request changes' feature if available
* The author should merge the patch after tests/review.
