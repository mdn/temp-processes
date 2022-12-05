# Pull request submission and review guidelines

This document describes how contributors make changes to MDN Web Docs and how the changes are reviewed and land on the site.

We strongly recommend opening pull requests that close existing issues or that are part of a bigger project. You can find tasks to help with under 'Issues' in any of the [MDN repositories](https://github.com/orgs/mdn/repositories) (for example, [Issues](https://github.com/mdn/content/issues) in `mdn/content` repository) and our public [project boards](https://github.com/orgs/mdn/projects).

Before embarking on any work in any of the MDN repositories, please make sure that you're not making changes that are already being made. You can do this by searching through the open 'Issues' and open 'Pull requests' in the repository you're interested in making changes.

If you are looking to suggest a new feature or a new set of work, please submit a proposal through the [suggestion form]().
Content changes to MDN Web Docs include:

- **Day-to-day improvements:** for the documentation of APIs, CSS properties, platform updates and content additions.
  This is usually done by MDN Web Docs staff working for Mozilla, Google, Open Web Docs, Samsung, but also by community volunteers.
- **Minor fixes:** and small updates to the site for fixing typos, grammatical issues, and technical inaccuracies.
  These issues are usually found by readers of MDN Web Docs.
- **Content bug fixes:** usually done by volunteers to close issues on the `mdn/content` repo.

Regardless of how content changes are done, they are submitted as pull requests on GitHub.
The content changes go through the following stages before they are published on MDN Web Docs:

1. **Submission:** As a pull request author, you [submit changes via opening a pull request](#opening-a-pull-request).
2. **Review:** Your changes are reviewed by [MDN members and volunteers](#pull-request-review-process).
3. **Publishing:** Updated content goes live within a day of merging via a site rebuild once every 24 hours.

## Values and participation

We want MDN Web Docs to be a welcoming, friendly community that we can all be proud of.
All participants must follow our [Code of Conduct](https://github.com/mdn/content/blob/main/CODE_OF_CONDUCT.md) which means adhering to [Mozilla's Community Participation Guidelines](https://www.mozilla.org/en-US/about/governance/policies/participation/).
Be polite and constructive when opening pull requests, writing review comments, interacting with the PR author or other community members.
If anyone has engaged in behavior that is potentially illegal or makes you or someone else feel unsafe, unwelcome, or uncomfortable, you are encouraged to [report it](https://www.mozilla.org/en-US/about/governance/policies/participation/reporting/).

## Opening a pull request

### If you find something you want to work on

Ideally you'll have found an issue or project task to work on before opening a pull request. Every pull request opened should be to close an existing issue. If you haven't check through issues on repos or public project boards to find something. If you have found a problem on MDN open an issue - more [information on issues can be found here](). **Issues need to be triaged before work can start.**

Make sure the issue isn't assigned and no one has already opened a pull request for the task. You can do that by checking the issue and searching open pull requests

If you're not sure where to start, reach out to us on [Discord]() and ask for feedback before starting on any work.

### Opening a pull request

When you're ready to open a pull request, follow these guidelines:

- **PRs should be short and focused to one issue:** If possible, group related set of changes into multiple, small PRs. If a PR becomes too large, the reviewer may close it and ask that you to submit pull requests for each logical set of changes that belong together.
- **Add a description of what the pull request is doing:** Provide as much context and reason for opening the pull request.
- **Add the link to the issue you are closing or working on** Add 'Fixes' or 'Relates to' and the related issue to the description of the pull request. See [github link here]()
- **Accompany code example changes with content changes** to ensure updated examples are served correctly.
  If content changes also affect how examples are used, the related code examples should be updated in associated repositories.
- **Add 'depends on'** with a link to a dependency if there are PRs that must land first (e.g. linked examples in other repos).
- **Add a reviewer** if you know who should review your PR already, such as a team member or a topic owner.
- **Don't make grammar-only changes.**
  MDN Web Docs contains technical documentation; you should not suggest prose style changes except where grammar is incorrect.
- **Don't enable auto-merge.**

### After you open a pull request

- **Handle CI failures** from the automated tests that run as GitHub Actions (see `.github/workflows`).
  If one or more of these tests fail, it is your responsibility to try to resolve them.
  If you don't know how to resolve the underlying issues, ask for help.
- **Resolve merge conflicts** with the main branch; you are responsible for resolving these.
  You can do this by merging the `mdn/main` branch into your branch.
  For more information, see the GitHub documentation on [keeping your branch up to date](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/keeping-your-pull-request-in-sync-with-the-base-branch#about-keeping-your-pull-request-in-sync).
- **Be responsive to feedback.**
  This means being prepared to make changes to the pull request based on the review.
  If a review happens and the changes are not made, the pull request may be closed.
- **Be patient during the review process.**
  The MDN organization receives a large volume of pull requests and the team may need time to review your contributions.
- **Don't reopen closed PRs.**
  If you must create a new PR, it can reference the closed one.

## Pull request review process

We add reviewers automatically based on a `CODEOWNERS` file but, if there is a specific person you want to request review from, manually [request a review](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review).
We also use auto-labeling on pull requests to help triage.
Maintainers will triage pull requests and add any additional labels if needed based on context. These are usually as and when are needed like `needs-info` or `on-hold`.

If you want to review a PR but are not listed as a reviewer, you may add yourself as one.
It's polite to check with existing reviewers first by commenting on the pull request that you intend to start a review.

When it comes to merging, the PR reviewer or an **assignee** merges the PR.

A note about reviewers and assignees. Reviewers are those that review the pull request and give feedback. Assignees are those that are assigned to do work on the pull request, either to reach a conclusion (either by merging or closing) or to undertake further work.

### If you are assigned to review a PR

Before you start with a review, check the PR description to make sure no one specific should review it.
Ensure that all continuous integration (CI) tasks have been completed successfully and that there are no merge conflicts.

If any tasks fail or there are merge conflicts, communicate this to the author; it is their responsibility to address these.
You may set the author as an **assignee** to indicate that a pull request needs their attention before a review can start.
Do leave the door open to the author to ask for help, especially new contributors to the project.

### Reviewing a pull request

When it comes to the changes in a pull request, content and prose must adhere to the [MDN Writing style guide](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide) and example code must follow the [code style guide](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide).

When you are reviewing a pull request, you should:

- **Add a comment** to the pull request to let the author know you are aware of the PR and will start the review.
  This is to avoid cases when someone else starts to review the PR at the same time unnecessarily.
- **Limit the scope of review** to the changes in the pull request only.
  Open a follow-up issue or PR to address other improvements not covered by the pull request.
- **Ask for help** and add the `review-help-needed` label if you need technical assistance with the review.
- **Close PRs with unrelated changes** if it is too complex or contains multiple unrelated changes.
  In such cases, ask the PR author to submit their changes in smaller chunks.
- **Request load balancing** if your plate is full and you don't have bandwidth for the review.
  Tag the `@core-yari-content` team and ask if someone else can step in.
- **Don't merge unless 'depends on'** PRs are merged first.

If a PR looks good apart from small typos or other minor issues, you may want to fix the problem directly.
You can do this provided the PR [has been set up to allow changes](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/allowing-changes-to-a-pull-request-branch-created-from-a-fork).
It's recommended to use [comments with suggestions](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/commenting-on-a-pull-request#adding-line-comments-to-a-pull-request) for fixing minor issues, as they can be batched and committed in one go.

When submitting your review you have three options, **approve**, **comment**, or **request changes**.
The following sections explain when to use each option.

#### Request changes

Use the request changes option when the feedback you provided _needs_ to be addressed by the author and re-reviewed by the reviewer before the pull request can be approved and merged.

#### Comment

Use the comment option when your feedback is not critical and will not require a re-review.
In short, you trust the author and other reviewers to use good judgment.

#### Approve

Use the approve option when everything looks good and is ready to merge from your perspective.
After submitting your review, you can safely merge the pull request if there are no other reviewers or any outstanding review comments to address.

#### What to do if you are stuck

If you don't understand a content change or feel that it is too large and complex for you to deal with, don't panic!
A good place to start is by asking for information from the PR author to help.

It is rare that you'll be required to review a large, complex content change with no warning.
If this does happen, however, the PR description should link to an issue that explains the background information.

If you are still not sure or if you think the content is suspicious, reach out to the MDN Web Docs team and ask for help.

## Reading list

Reviewers are encouraged to read the following articles for help with common reviewer tasks:

- [The Art of Closing: How to closing an unfinished or rejected pull request](https://blog.jessfraz.com/post/the-art-of-closing/)
- [Kindness and Code Reviews: Improving the Way We Give Feedback](https://product.voxmedia.com/2018/8/21/17549400/kindness-and-code-reviews-improving-the-way-we-give-feedback)
- [Code Review Guidelines for Humans: Examples of good and back feedback](https://phauer.com/2018/code-review-guidelines/#code-reviews-guidelines-for-the-reviewer)

## Timelines

This section provides details for expected turnaround times while reviewing PRs if you're a reviewer and while responding to review comments if you're a PR author.

- **Reviews**:
  The assigned reviewer should be able to review the PR in 2 weeks or less.
  In the 2 weeks after the PR is open, the assigned reviewer can:
  - Leave a comment about when they can start reviewing the PR
  - Ask for technical or resource help
- **Addressing requested changes:**
  The PR author should be able to respond to or fix the comments in 4 weeks or less.
  If the PR author is unable to respond or fix the review comments in that time, the reviewer can do one of the following:
  - Commit the changes and merge the PR
  - Close the PR

## External reviewers

Some PRs on the MDN content repo relate to specific work by browser vendors or organizations with defined authors and reviewers.
The author will include the username of the reviewer in a line at the bottom of the pull request description in these cases, for example:

```md
reviewer: @jpmedley
```

If you receive a review request and you have been overridden with another reviewer in the manner described above, do not review the changes.
Once the reviewer mentioned in the description has approved the changes, they will ask for an approval required by the `CODEOWNERS`.
