---
title: Guidelines to open, triage, and work on issues
slug: MDN/Community/Issues
page-type: mdn-community-guide
tags:
  - meta
  - community-guidelines
  - governance
---

{{MDNSidebar}}

As a contributor, you can [report](#Guidelines_for_reporting_an_issue) and [work](#guidelines_for_working_on_an_issue) on issues.

After you report an issue, the issue gets triaged. Issue [triaging](#guidelines_for_triaging_issues) is typically done by people assigned the role of a maintainer or an owner.

## General guidelines for participation

While reporting an issue or participating in a conversation in an issue, always ensure that your inputs are contributing to the overall progress of the project. Consider whether the issues you open and your comments in an issue are constructive and on topic and are not just adding noise.

Do the following:

- Before filing an issue, consider if you need to start a [discussion](https://github.com/mdn/mdn-community/discussions) in the MDN project on GitHub. Use discussions to gain different viewpoints and to converge on an agreed upon course of action. This helps to keep issues focused and productive.
- Before filing an issue, read our [contribution guide](https://github.com/mdn/content/blob/main/CONTRIBUTING.md) to try to fix the problem yourself.
- If you have a question, you can ask using mechanisms like [chat rooms](https://chat.mozilla.org/#/room/#mdn:mozilla.org) or [forums](https://discourse.mozilla.org/c/mdn/236) without filing an issue.

Avoid doing the following:

- Complicating issues by trying to discuss multiple topics or by making off-topic comments.
- Opening lots of issues asking vague questions.
- Asking questions without trying to solve the problem yourself first.

## Guidelines for reporting an issue

[Issues](https://docs.github.com/en/github/managing-your-work-on-github/about-issues) are used to track bugs. An issue must be a single actionable task or a collection of multiple, related actionable tasks and must have a clear actionable outcome.

### Before filing an issue

If you've found a bug with either the content on MDN or the platform, search the current open issues in the [relevant repository](/en-US/docs/MDN/Community/Contributing/Our_repositories) to ensure that someone has not already reported the issue.

### Reporting an issue

- Depending on the problem you've discovered, report it by filing a [documentation issue](https://github.com/mdn/content/issues), a [localization issue](https://github.com/mdn/translated-content/issues), or a [platform issue](https://github.com/mdn/yari/issues).

- To open an issue, use the appropriate template available in the repository. For example, to report a content bug, use the the [Content issue](<https://github.com/mdn/content/issues/new?assignees=&labels=needs+triage&template=content-bug.yml>) template in the `mdn/content` repository.

- Provide sufficient information while reporting the issue:

  - **Issue title** must convey succinctly the _required action_.

  - **Issue description** must clearly describe the bug and the action required to resolve the issue. It must also list the task or sub-tasks to be completed to resolve the issue. Some other guidelines include:
    - Use the description field to indicate the status of the task or sub-tasks by using checklists.
    - Updates to the status of a task should be conveyed by editing the task list in the issue description instead of adding a new comment. One should not have to scroll through comments or replies to find the status of a task or sub-task.
    - Comments in an issue should be limited to details or context that help resolve the issue.

- If the information you provide in the issue is incomplete, then you might be contacted later during the [issue triaging process](#review_issue_to_determine_completeness_of_information).

- If you find yourself in one of the following situations, move the conversation to [MDN's discussion on GitHub](https://github.com/mdn/mdn-community/discussions):
  - A discussion needs to take place to clarify an issue.
  - A discussion begins after opening the issue.
  - The issue has no clear consensus on its resolution.
  - The requirements for completing the task expand while it's being resolved or the work is unclear.

- You can open an issue and [fix it yourself](#fixing_issues_yourself).

### Creating an issue task tracker

If the issue you're opening is not to report a bug but to perform a series of tasks, you can create the issue as a tracker.
Explain the context or reason for performing the tasks in the description.
Ensure that you list all the actionable tasks as a checklist.

For example:

   ```markdown
   // Issue title
   Ensure sections follow the order defined in the CSS property template

   // Issue description
   The CSS property page template is defined [here](/en-US/docs/MDN/Writing_guidelines/Page_structures/Page_types/CSS_property_page_template).
   This issue tracker will be used to compare the documented CSS properties with the template and track changes to the property pages for compliance.

   ### List of pages checked

   - [x] [accent-color](/en-US/docs/Web/CSS/accent-color) - checked, okay
   - [ ] [backdrop-filter](/en-US/docs/Web/CSS/backdrop-filter)
   - [ ] [letter-spacing](/en-US/docs/Web/CSS/letter-spacing) - open pull request to move `Accessibility concerns` and `Internationalization concerns` sections before the `Specifications` section.
   ```

## Guidelines for working on an issue

Remember that if you take on an issue, the expectation is for the work to be completed in a timely manner. If you can no longer complete the required task, leave a comment and unassign yourself from the issue.

These are the general steps for working on an issue:

1. **Find an issue:** If you're looking to contribute, search for issues with `help wanted` or `good first issue` label. Most repositories have issues with these labels. You are welcome to browse and pick an issue that is suitable for your skill set.

   > **Note:** An issue with the `needs triage` label indicates that the MDN core team has not reviewed the issue yet, and you shouldn't begin work on it.

2. **Assign yourself to the issue:** After finding an issue you'd like to work on, make sure no one else is assigned to the issue. Add a comment saying you would like to work on it, and assign the issue to yourself.

3. **Do the research:** Most issues need some investigation before work can start.

   - Scope out the work that needs to be done. If you need to ask questions, ask for help in the [MDN Web Docs chat room](https://chat.mozilla.org/#/room/#mdn:mozilla.org) on [Matrix](https://wiki.mozilla.org/Matrix).
   - If the issue is well-described, and the work is pretty obvious, go ahead and do it.
   - If the issue is not well-described, and/or you are not sure what is needed, feel free to @mention the poster and ask for more information.
   - If you are not still sure who to ask, ask for help in the [MDN Web Docs chat room](https://chat.mozilla.org/#/room/#mdn:mozilla.org) on [Matrix](https://wiki.mozilla.org/Matrix).

4. **Make the changes:** Fork and branch the repository. Do your work and open a [pull request](/en-US/docs/MDN/Community/Pull_requests) in the repository. Comment in the issue and ask for a review of your pull request.

   If you no longer have the time to work on the assigned issue, let the team know in a comment so that the issue can be assigned to someone else.

5. After your pull request has been reviewed and merged, you can mark the linked issue as closed. If you opened the pull request with `Fixes #<issue>` verbiage, the issue will be closed automatically when the pull request is merged.

### Fixing issues yourself

If you spot a bug — whether it's a problem with site infrastructure or an error in documentation — you can try to fix it yourself.

[Report the problem](#guidelines_for_reporting_an_issue) as described earlier.

You can fix the problem yourself by updating the appropriate source:

- The MDN content (in English) is found in the [content](https://github.com/mdn/content) repository.
- The MDN content translated in other locales is found in the [translated-content](https://github.com/mdn/translated-content) repository.
- The MDN platform code, which renders the content as MDN, is found in the [yari](https://github.com/mdn/yari) repository.

Each repository includes useful information to guide you on how to contribute.

## Guidelines for triaging issues

If you are a maintainer or an owner in the MDN GitHub organization, you are responsible for triaging issues in one or more MDN repository.

The overall process for triaging includes some [general](#general_triaging_tasks) and some [issue-specific tasks](#issue_specific_triaging_tasks).

### General triaging tasks

- When an issue is opened, the `needs triage` label is set on the issue automatically. You can search for this label to look for issues that [need to be triaged](#issue_specific_triaging_tasks). Contributors or anybody else should not work on the issue until the issue has been triaged. (Triagers should remember to remove the `needs triage` label after triaging the issue.)

- In the [mdn/content repository](https://github.com/mdn/content/issues), an additional `Content:` label, such as `Content:CSS` or `Content:WebAPI`, is set on the issue automatically. This gets set based on the MDN URL mentioned in the issue. You can use the content-specific label to look for issues to be triaged in your specific topic area.

- If an issue concerns an active, non-en-US locale, set the appropriate label, such as `l10n-fr`, `l10n-zh`, or `l10n-ja`. The teams for those locales will pick these issues up and triage them.

- You don't need to actively triage issues all the time. Set aside time, say 30 minutes every week, to triage issues on a regular basis in your area of responsibility. Triaging doesn't have to be done as part of a synchronous meeting or even at the same time as everyone else, but it should be done regularly to make sure that the backlog of untriaged bugs doesn't get too high.

- Apart from triaging incoming issues every week, review the list of old bugs to see if there are any that are stalled, need closing, or are no longer relevant.
  - Check assigned issues that are still open to see if the assignee is making progress. If there is no progress after a week of being assigned, ask them if they still have time to work on the issue. If another week passes by without any progress, unassign them and leave a comment indicating that you're making the issue available for other interested contributors.
  - If a pull request has been opened to fix the issue but has not been reviewed for a week, give the reviewer a gentle ping to ask if they can get to it.
  - If a pull request to fix the issue is waiting on review comments to be addressed after a week, then ask the submitter if they can respond to their review. If another week goes by, either fix the review comments yourself if you have time, or close the pull request and unassign the related issue.

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

### Issue-specific triaging tasks

These are the guidelines to follow while triaging each issue.

#### Review the issue to determine the completeness of information

Review each issue against the following checklist to ensure that the issue contains the described information for someone to start working on the bug:

- MDN URL where the problem has been found.
- The specific heading or section on the MDN page where the problem can be found.
- URL of an example page or repository related to the bug, if appropriate.
- A clear description of what the problem is.

If any of the above information is not present, then you should ask the submitter of the issue to provide these details and resume triaging the issue only after those details have been provided.

#### Set a priority label

For each bug, set a priority label based on the severity of the issue to help people who want to work on the most important issues or areas.

- Critical issue: This type of issue needs to be fixed as soon as possible, regardless of where it appears on the site. This type of issue could damage MDN's reputation severely and/or harm users. Examples of this issue include an incorrect code snippet, which if used in production, could create a severe security problem and undesirable content such as malware, profanity, pornography, hate speech, or links to such content.
  - Label: `p0` (will be addressed immediately)

- Major issue: This type of issue could severely affect a page's usefulness. For example, a significant amount of out-of-date information, a complex and important code example that doesn't work, a significant amount of prose that is badly written and hard to understand, or a large number of broken links.
  - Labels: `p1` (will be addressed soon) and `p2` (will be addressed soon, but higher priority items will take precedence)

- Minor issue — This is a type of improvement issue that can make the existing content better but does not affect learning or only has a minor effect on learning. Examples include typos, bad grammar, a broken link, a small amount of out-of-date information or badly-written prose, or a code snippet that doesn't work.
  - Labels: `p3` (no visibility when the issue will be addressed)

In general, critical issues should be fixed immediately and are most likely handled by MDN staff and peers.

#### Add helpful information

If possible, add information that can help contributors to fix the issue. The information can be in the form of steps, direction, or reading resources. You can time-box this task to 5 minutes.

For example, as a triager, you can add the following information to the issue you are triaging:

```plain
To whoever fixes this issue, it looks like the following is needed:

* Update the first paragraph below heading X to correct the problem with Y
* Add a description of X
* Update the compatibility data at Link-X
```

#### Set other labels

Next, set the following labels as appropriate:

- `effort: small`, `effort: medium`, `effort: large`: Some contributors like to search for bugs based on the time and effort that will be needed to fix the bug. So where possible, you should try to provide an estimate of the required effort.
- `good first issue`: Set this label on the issue if the fix for the issue is really simple and if fixing the issue would provide good practice for a newcomer who is getting used to the process.
- `help wanted`: Set this label if the issue requires help from someone who knows about or is familiar with the topic. This is a popular label and some contributors use it to search for issues to work on in open source projects in their areas of familiarity or expertise.
- `broken link internal`, `broken link external` — Set the appropriate label if the issue involves a link to a non-existent internal page or a broken external link.
- `needs content update`: Set this label if the issue fix in another repository will need an equivalent fix in the `mdn/content` repository.

   > **Note:** After the triage process is complete, remove the `needs triage` label.
