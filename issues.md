# Guidelines for reporting, triaging, and working on issues

As a contributor, you can report and work on an issue. Triaging is typically done by people assigned the role of maintainers and owners.

## General participation guidelines

While reporting an issue or participating in a conversation, always ensure that your inputs are contributing to the overall progress of the project. Consider whether your issues and comments are on topic or if they are just adding noise.

Dos:

- Use [discussions](https://github.com/mdn/mdn-community/discussions) in the MDN project on GitHub before filing an issue. Use discussions to gain different viewpoints and to converge on an agreed upon course of action. This helps to keep issues focused and productive.
- If you have a simple question, you can ask using other mechanisms like [chat rooms](https://chat.mozilla.org/#/room/#mdn:mozilla.org) or [forums](https://discourse.mozilla.org/c/mdn/236) without filing an issue.
- Read our [contribution guidelines](/en-US/docs/MDN/Community) and [writing guidelines](/en-US/docs/MDN/Writing_guidelines) first to try to solve the issue yourself.

Don'ts:

- Complicate issues by trying to discuss multiple topics or by making off-topic comments.
- Open lots of issues asking vague questions.
- Ask questions without trying to solve the problem yourself first.

## Issue reporting guidelines

[Issues](https://docs.github.com/en/github/managing-your-work-on-github/about-issues) are used to track bugs. An issue must be a single actionable task or a collection of multiple, related actionable tasks and must have a clear actionable outcome.

### Before filing an issue

If you've found a bug with either the content on MDN or the platform, search the current open issues in the [relevant repository](/en-US/docs/MDN/Community/Contributing/Our_repositories) to ensure someone has not already reported the issue.

### While filing an issue

- To open an issue, use the appropriate template available in the repository.

- Ensure that the issue description clearly states the bug and the action required to resolve the issue. Follow these guidelines while reporting a bug:

  - **Issue title:** Must convey succinctly the required action.

  - **Issue description:** Must list the task or sub-tasks to be completed to resolve the issue.

    - Use the description field to indicate the completion and outstanding status of the task or sub-tasks by using checklists. Updates to the status of a task should be done by editing the issue description or the task list instead of in a comment. One should not have to scroll through comments or replies to find the status of a task or sub-tasks.
    - Comments in an issue should be limited to details or context that help resolve the issue. If you find yourself in one of the following situations, move the conversation to [MDN's GitHub discussions](https://github.com/mdn/mdn-community/discussions):
      - A discussion needs to take place to clarify an issue
      - A discussion begins after opening the issue
      - The issue has no clear consensus on its resolution
      - The requirements for completing the task expand while it's being resolved or the work is unclear

- If the issue you're filing is not to report a bug, you can create an issue tracker. Ensure that you list the actionable tasks or a clear outcome in the issue tracker. Also explain the context or reason for performing the tasks. For example:

   ```markdown
   ## Remove \{{ warning }} macro from documents

   We should no longer be using the `\{{ warning }}` macro in our documentation because it has been deprecated.

   ### Task description

   We should replace all instances of the `\{{ warning }}` macro with the following:

   > **Warning:** Main subject line
   >
   > Details of the warning.
   > It can have multiple paragraphs.

   ### Actionable outcome

   - [ ] There are no more instances of the `\{{ warning }}` macro in the `mdn/content` repository.
   - [ ] Deprecate `\{{ warning }}` macro
   - [ ] Notify localization team leads of the change.
   ```

## Working on an issue

Remember that if you take on an issue, the expectation is for work to be completed in a timely manner. If you can no longer complete the required task, leave a comment and unassign yourself from the issue.

These are the general steps for working on an issue:

1. If you're looking to contribute, search for issues with `help wanted` or `good first issue` label. Most repositories have issues with these labels; some do not, but this is not a pre-requisite. You are welcome to browse and pick an issue that is suitable for your skill set.

   > **Note:** An issue with the `needs triage` label indicates that the team has not reviewed the issue yet, and you shouldn't begin work on it.

2. After finding an issue you'd like to work on, make sure no one else is assigned to the issue. Add a comment saying you would like to work on it, and assign the issue to yourself.

   Most issues need some investigation before work can start. If you need to ask questions, ask for help in the [MDN Web Docs chat room](https://chat.mozilla.org/#/room/#mdn:mozilla.org) on [Matrix](https://wiki.mozilla.org/Matrix).

3. Fork and branch the repository. Do your work and open a [pull request](/en-US/docs/MDN/Community/Pull_requests) in the repository.

### Troubleshooting problems

If you run into problems — whether it's a problem with site infrastructure or an error in documentation content — you can try to fix it yourself, report the problem (file an issue), or ask in Discord.

The best thing you can possibly do is fix problems you spot yourself — this is done by updating the site source:

- The MDN content itself (in English) is found in the [content](https://github.com/mdn/content) repository.
- The MDN content, translated in other locales, is found in the [translated-content](https://github.com/mdn/translated-content) repo.
- The MDN platform code, which renders the content as MDN, is found in the [yari](https://github.com/mdn/yari) repo.

Each repository includes useful information to guide you on how to contribute.

However, maybe you don't know the answer or are in the middle of a deadline on your own project, and need to jot down the problem so someone can look at it later.

The way to report a documentation problem by filing an [documentation issue](https://github.com/mdn/content/issues), [localization issue](https://github.com/mdn/translated-content/issues) or [platform issue](https://github.com/mdn/yari/issues), depending on what the problem you've discovered relates to.

## When choosing a GitHub issue to work on

1. Write a comment in the issue saying that you would like to take it on, and we'll assign you to it.

   - If someone else is already assigned to the issue:

     1. If this was more than one week ago, and there has not been much activity, @mention them and ask them if you can take it over, or otherwise help get it to completion.

        - If they agree for you to take it, we'll assign you to it and remove them.
        - If they agree for you to take it and some work has been done already, or the agreement is to help them out with it, we'll assign you to it alongside them.

     2. If it was less than one week ago, then have some patience, and give them a chance to work on it.

2. If the issue has been marked as complete but needing a review, and you want to review it, @mention them in the comments and say you'll review it.

## When you've been assigned to an issue

1. Scope out the remainder of the work that needs to be done.

   - If the issue is well-described, and the work is pretty obvious, go ahead and do it.
   - If the issue is not well-described, and/or you are not sure what is needed, feel free to @mention the poster and ask for more information.
   - If you are not still sure who to ask, ask for help in the [MDN Web Docs chat room](https://chat.mozilla.org/#/room/#mdn:mozilla.org) on [Matrix](https://wiki.mozilla.org/Matrix).

2. Once you think you've fixed an issue, ask for a review in the comments.
3. Once an issue has been successfully reviewed and comments answered, you can mark it as closed.
4. If you no longer have time to work on an issue, let us know in a comment so we can assign it someone else.

This document looks at the process for triaging content bugs and getting them ready for contributors to effectively work on.

## Reporting and working on bugs

Anyone can report a content bug by writing an issue at <https://github.com/mdn/content/issues/new> using the "Content bug" issue template, or by using the "Report a problem with this content on GitHub" link at the bottom of each MDN page.

Once reported, content bugs are listed at <https://github.com/mdn/content/issues>, and are designed to be done by individuals with minimal process requirements. Anyone is welcome to work on a content bug, using the process outlined at [Fixing MDN content bugs](/en-US/docs/MDN/Community/Issues).

## Overall triage process

At a high level, the process for triage looks like so:

Triage preparation:

- Decide on triagers — Who will do the regular triage?
- Set initial labels — As soon as a new bug comes in, give it the "needs-triage" label, to signify that it needs to be triaged (this should happen automatically), plus a "Content:" label to signify what topic area it is in, e.g. "Content:HTML". Anyone can do this as they spot bugs coming in, but the MDN core team will keep an active eye on this.
- Set aside triage time — set out a regular 30-minute slot in which to do the triage, each week.

Triage for each issue:

- Checklist — run through checklist to see if it is ready to triage.
- Set priority measure — according to priority rules.
- Provide further information to help other contributors start working on bugs more easily.
- Set other labels — there are other labels to set, to help people to choose issues to work on.

Check through old bugs — look at existing bugs, and see if there are any that are stalled, or need closing, etc.

## Triage preparation

### Decide on triagers

We need an assigned triager to regularly triage bugs coming in on each MDN content area. We currently have the following triagers assigned:

- Accessibility — Eric Bailey?
- CSS — Rachel Andrew
- DevTools — Hamish Willee
- HTML — Rachel Andrew
- HTTP — Florian Scholz
- JS — Florian Scholz
- Learn — Chris Mills
- Learn:CSS — Rachel Andrew
- Learn:Express / Learn:Django — Hamish Willee
- Media — Ruth John
- Other — Ruth John
- SVG — André Jaenisch
- WebAPI — Ruth John
- WebExt — Caitlin/WebExt team

### Set initial labels

As soon as a new issue is filed, the MDN core team, and anyone else who wishes to help, will add the following labels to that issue:

- `needs-triage` — signals that this issue needs a proper triage, to get it ready to work on (this should happen automatically).
- `Content:<area>` — specifies the content topic this issue relates to, e.g. `Content:HTML` or `Content:CSS`. This needed for the triagers to be able to find the issues in their specific areas.
- `l10n-fr`, `l10n-zh`, `l10n-ja` — specifies that the issue filed concerns an active non-en-US locale. The teams for those locales will pick these issues up and triage them.

### Set aside triage time

Triagers don't need to be actively triaging bugs all the time. Instead, they should set out a 30-minute slot in which to triage the bugs in their area of responsibility, each week.

This doesn't have to be done as part of a synchronous meeting, or even at the same time as everyone else, but it should be done regularly, say once per week, to make sure that the backlog of untriaged bugs doesn't get too high.

## Triage process for each issue

### Checklist to determine if we have enough information

For each bug, run through the following checklist to make sure the issue contains enough information for someone to start working on the bug.

Does the issue contain:

- The MDN URL where the problem has been found.
- The URL of any example page or repository related to the bug, if appropriate.
- The specific heading on the MDN page where the problem can be found (if needed to find it).
- A clear description of what the problem is.

If this information is not present, then the triager should ask the submitter of the issue to provide these details, and not continue triaging the issue until those details are provided.

### Set priority measure

For each bug, set a priority measure label to help people who want to work on the most important issues or areas (rather than the topics they are interested in).

The levels of priority are:

- `P0` — A critical issue on any MDN doc.
- `P1` — A major issue on a Tier 1 MDN doc.
- `P2` — A minor issue on a Tier 1 MDN doc.
- `P3` — A major issue on a Tier 2 MDN doc.
- `P4` — A minor issue on a Tier 2 MDN doc.

Definitions:

- Critical issue — Something that could damage MDN's reputation severely and/or harm users, which we need to fix as soon as possible, regardless of where it appears on the site. Examples include code examples that if used in production could create a severe security issue, undesirable content such as malware, profanity, pornography, hate speech, or other undesirable content, or links to such content.
- Major issue — Something that could severely affect a page's usefulness, for example a significant amount of out-of-date information, a complex and important code example that doesn't work, a significant amount of prose that is badly written and hard to understand, a large number of broken links, etc.
- Minor issue — something that doesn't look great but does not affect learning, or only has a minor effect on learning. Examples — Typos, bad grammar, a broken link, a small amount of out-of-date information or badly-written prose, a small code snippet that doesn't work.

Generally speaking, critical issues should be fixed immediately, and would probably be handled by MDN staff/peers.

### Provide further information

It is really useful for other contributors to provide them with further information to help them fix issues; we'd like to recommend that triaging each bug involves a time-box of up to 5 minutes in which the triager quickly describes some steps to take to fix the bug, to help the person who eventually tries to fix it.

For example:

```plain
To whoever fixes this issue, it looks like the following is needed:

* Update the first paragraph below heading X to correct the problem with Y
* Add a description of X
* Update the compatibility data at Link-X
```

### Set other labels

Next, set other labels as appropriate:

- `10 minute task`, `30 minute task`, `1 hour task`, `multiple hour task` — Some people like to search for bugs based on how much time they've got to contribute, so we like to give a rough measure to allow people to choose. We appreciate that this is hard to estimate, and that different people will fix bugs at different speeds, but this is only supposed to be a rough measure. When setting it, think about how much time you think someone with a moderate-to-good amount of knowledge in the subject area would take to fix it.
- `good first issue` — if the fix for the issue is really simple, and it would be a good practice issue for a newcomer just getting used to the system, mark it with this label.
- `help wanted` — this seems to be a very popular label for people to use to search for things to do on open source projects, so we set this as a matter of course on successfully-triaged bugs.
- `broken-link-internal`, `broken-link-external` — use these if the issue involves a link to a non-existent internal page, or a broken external link.
- Once the triage process is completed, **don't forget to remove the `needs-triage label`.**

## Check through old issues

At the end of your triage session, have a look through the older existing triaged issues in your topic area, and check to make sure none of the issues are being unnecessarily stalled or clogged up:

- Check assigned issues that are still open to see if the assignee is making progress. If they have done nothing after a week of being assigned, ask them if they still have to work on the issue. If another week passes and they have still done nothing, unassign them and say that you are opening this up again for others to take.
- If a PR has been issued to fix the issue but it has not been reviewed for a week, give the reviewer a gentle ping to ask if they can get to it.
- If a PR is waiting on review comments to be addressed after a week, then ask the submitter if they can respond to their review. If another week goes by, either fix the review comments yourself if you have time, or close the PR if not.
