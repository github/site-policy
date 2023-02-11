Parameters
Many quick actions require a parameter. For example, the /assign quick action requires a username. GitLab uses autocomplete characters with quick actions to help users enter parameters, by providing a list of available values.
          for issue_url in $(gh list-reports \
                                  --search 'no:assignee' \
                                  --json url \
                                  --jq '.[].url'); do
            if [ "$issue_url" != "${{ env.NEW_REPORT_URL }}" ]; then
              gh issue comment $issue_url --body "➡️ [Newer report](${{ env.NEW_REPORT_URL }})"
              gh issue close $issue_url
              gh issue edit $issue_url --remove-project "${{ env.FIRST_RESPONDER_PROJECT }}"
            fi
          done
If you manually enter a parameter, it must be enclosed in double quotation marks ("), unless it contains only these characters:

GitLab documentation home
Docs
What's new?
GitLab Docs
Learn GitLab with tutorials
Manage GitLab subscription
Install GitLab
Install GitLab Runner
Administer GitLab
Use GitLab
Set up your organization
Organize work with projects
Plan and track work
Labels
Iterations
Milestones
Issues
Comments and threads
Tasks
Requirements
Time tracking
Customer relations (CRM)
Wikis
Epics
Roadmaps
Planning hierarchies
Objectives and key results (OKR)
Keyboard shortcuts
Quick actions
Autocomplete characters
Markdown
To-Do List
Using Git
Build your application
Secure your application
Deploy and release your application
Monitor application performance
Monitor runner performance
Manage your infrastructure
Analyze GitLab usage
Develop with GitLab
Contribute to GitLab development
GitLab quick actions ALL TIERS
Version history 
Quick actions are text-based shortcuts for common actions that are usually done by selecting buttons or dropdowns in the GitLab user interface. You can enter these commands in the descriptions or comments of issues, epics, merge requests, and commits.

Many quick actions are context-aware, requiring certain conditions be met. For example, to remove an issue due date with /remove_due_date, the issue must have a due date set.

Be sure to enter each quick action on a separate line to allow GitLab to properly detect and execute the commands.

Parameters
Many quick actions require a parameter. For example, the /assign quick action requires a username. GitLab uses autocomplete characters with quick actions to help users enter parameters, by providing a list of available values.

If you manually enter a parameter, it must be enclosed in double quotation marks ("), unless it contains only these characters:

ASCII letters
Numbers (0-9)
Underscore (_), hyphen (-), question mark (?), dot (.), ampersand (&) or at (@)
Parameters are case-sensitive. Autocomplete handles this, and the insertion of quotation marks, automatically.

Issues, merge requests, and epics
The following quick actions are applicable to descriptions, discussions, and threads. Some quick actions might not be available to all subscription tiers.

Command	Issue	Merge request	Epic	Action
/add_contacts [contact:email1@example.com] [contact:email2@example.com]	 Yes	 No	 No	Add one or more active CRM contacts (introduced in GitLab 14.6).
/approve	 No	 Yes	 No	Approve the merge request.
/assign @user1 @user2	 Yes	 Yes	 No	Assign one or more users.
/assign me	 Yes	 Yes	 No	Assign yourself.
/assign_reviewer @user1 @user2 or /reviewer @user1 @user2 or /request_review @user1 @user2	 No	 Yes	 No	Assign one or more users as reviewers.
/assign_reviewer me or /reviewer me or /request_review me	 No	 Yes	 No	Assign yourself as a reviewer.
/award :emoji:	 Yes	 Yes	 Yes	Toggle emoji award.
/cc @user	 Yes	 Yes	 Yes	Mention a user. In GitLab 15.0 and later, this command performs no action. You can instead type CC @user or only @user. In GitLab 14.9 and earlier, mentioning a user at the start of a line created a specific type of to-do item notification.
/child_epic <epic>	 No	 No	 Yes	Add child epic to <epic>. The <epic> value should be in the format of &epic, group&epic, or a URL to an epic (introduced in GitLab 12.0).
/clear_health_status	 Yes	 No	 No	Clear health status (introduced in GitLab 14.7).
/clear_weight	 Yes	 No	 No	Clear weight.
/clone <path/to/project> [--with_notes]	 Yes	 No	 No	Clone the issue to given project, or the current one if no arguments are given (introduced in GitLab 13.7). Copies as much data as possible as long as the target project contains equivalent labels, milestones, and so on. Does not copy comments or system notes unless --with_notes is provided as an argument.
/close	 Yes	 Yes	 Yes	Close.
/confidential	 Yes	 No	 Yes	Mark issue or epic as confidential. Support for epics introduced in GitLab 15.6.
/copy_metadata <!merge_request>	 Yes	 Yes	 No	Copy labels and milestone from another merge request in the project.
/copy_metadata <#issue>	 Yes	 Yes	 No	Copy labels and milestone from another issue in the project.
/create_merge_request <branch name>	 Yes	 No	 No	Create a new merge request starting from the current issue.
/done	 Yes	 Yes	 Yes	Mark to do as done.
/draft	 No	 Yes	 No	Set the draft status. Use for toggling the draft status (deprecated in GitLab 15.4.)
/due <date>	 Yes	 No	 No	Set due date. Examples of valid <date> include in 2 days, this Friday and December 31st. See Chronic for more examples.
/duplicate <#issue>	 Yes	 No	 No	Close this issue. Mark as a duplicate of, and related to, issue <#issue>.
/epic <epic>	 Yes	 No	 No	Add to epic <epic>. The <epic> value should be in the format of &epic, group&epic, or a URL to an epic.
/estimate <time> or /estimate_time <time>	 Yes	 Yes	 No	Set time estimate. For example, /estimate 1mo 2w 3d 4h 5m. Learn more about time tracking. Alias /estimate_time introduced in GitLab 15.6.
/health_status <value>	 Yes	 No	 No	Set health status. Valid options for <value> are on_track, needs_attention, and at_risk (introduced in GitLab 14.7).
/invite_email email1 email2	 Yes	 No	 No	Add up to six email participants. This action is behind feature flag issue_email_participants and is not yet supported in issue templates.
/iteration *iteration:"iteration name"	 Yes	 No	 No	Set iteration. For example, to set the Late in July iteration: /iteration *iteration:"Late in July" (introduced in GitLab 13.1).
/label ~label1 ~label2 or /labels ~label1 ~label2	 Yes	 Yes	 Yes	Add one or more labels. Label names can also start without a tilde (~), but mixed syntax is not supported.
/lock	 Yes	 Yes	 No	Lock the discussions.
/link	 Yes	 No	 No	Add a link and description to linked resources in an incident (introduced in GitLab 15.5).
/merge	 No	 Yes	 No	Merge changes. Depending on the project setting, this may be when the pipeline succeeds, or adding to a Merge Train.
/milestone %milestone	 Yes	 Yes	 No	Set milestone.
/move <path/to/project>	 Yes	 No	 No	Move this issue to another project. Be careful when moving an issue to a project with different access rules. Before moving the issue, make sure it does not contain sensitive data.
/parent_epic <epic>	 No	 No	 Yes	Set parent epic to <epic>. The <epic> value should be in the format of &epic, group&epic, or a URL to an epic (introduced in GitLab 12.1).
/promote	 Yes	 No	 No	Promote issue to epic.
/promote_to_incident	 Yes	 No	 No	Promote issue to incident (introduced in GitLab 14.5). In GitLab 15.8 and later, you can also use the quick action when creating a new issue.
/page <policy name>	 Yes	 No	 No	Start escalations for the incident (introduced in GitLab 14.9).
/publish	 Yes	 No	 No	Publish issue to an associated Status Page (Introduced in GitLab 13.0)
/ready	 No	 Yes	 No	Set the ready status (Introduced in GitLab 15.1).
/reassign @user1 @user2	 Yes	 Yes	 No	Replace current assignees with those specified.
/reassign_reviewer @user1 @user2	 No	 Yes	 No	Replace current reviewers with those specified.
/rebase	 No	 Yes	 No	Rebase source branch. This schedules a background task that attempts to rebase the changes in the source branch on the latest commit of the target branch. If /rebase is used, /merge is ignored to avoid a race condition where the source branch is merged or deleted before it is rebased. If there are merge conflicts, GitLab displays a message that a rebase cannot be scheduled. Rebase failures are displayed with the merge request status.
/relabel ~label1 ~label2	 Yes	 Yes	 Yes	Replace current labels with those specified.
/relate #issue1 #issue2	 Yes	 No	 No	Mark issues as related.
/remove_child_epic <epic>	 No	 No	 Yes	Remove child epic from <epic>. The <epic> value should be in the format of &epic, group&epic, or a URL to an epic (introduced in GitLab 12.0).
/remove_contacts [contact:email1@example.com] [contact:email2@example.com]	 Yes	 No	 No	Remove one or more CRM contacts (introduced in GitLab 14.6).
/remove_due_date	 Yes	 No	 No	Remove due date.
/remove_epic	 Yes	 No	 No	Remove from epic.
/remove_estimate or /remove_time_estimate	 Yes	 Yes	 No	Remove time estimate. Alias /remove_time_estimate introduced in GitLab 15.6.
/remove_iteration	 Yes	 No	 No	Remove iteration (introduced in GitLab 13.1).
/remove_milestone	 Yes	 Yes	 No	Remove milestone.
/remove_parent_epic	 No	 No	 Yes	Remove parent epic from epic (introduced in GitLab 12.1).
/remove_time_spent	 Yes	 Yes	 No	Remove time spent.
/remove_zoom	 Yes	 No	 No	Remove Zoom meeting from this issue.
/reopen	 Yes	 Yes	 Yes	Reopen.
/severity <severity>	 Yes	 No	 No	Set the severity. Issue type must be Incident. Options for <severity> are S1 … S4, critical, high, medium, low, unknown. Introduced in GitLab 14.2.
/shrug <comment>	 Yes	 Yes	 Yes	Append the comment with ¯\＿(ツ)＿/¯.
/spend <time> [<date>] or /spend_time <time> [<date>]	 Yes	 Yes	 No	Add or subtract spent time. Optionally, specify the date that time was spent on. For example, /spend 1mo 2w 3d 4h 5m 2018-08-26 or /spend -1h 30m. Learn more about time tracking. Alias /spend_time introduced in GitLab 15.6.
/submit_review	 No	 Yes	 No	Submit a pending review (introduced in GitLab 12.7).
/subscribe	 Yes	 Yes	 Yes	Subscribe to notifications.
/tableflip <comment>	 Yes	 Yes	 Yes	Append the comment with (╯°□°)╯︵ ┻━┻.
/target_branch <local branch name>	 No	 Yes	 No	Set target branch.
/title <new title>	 Yes	 Yes	 Yes	Change title.
/timeline <timeline comment> \| <date(YYYY-MM-DD)> <time(HH:MM)>	 Yes	 No	 No	Add a timeline event to this incident. For example, /timeline DB load spiked \| 2022-09-07 09:30. (introduced in GitLab 15.4).
/todo	 Yes	 Yes	 Yes	Add a to-do item.
/unapprove	 No	 Yes	 No	Unapprove the merge request. (introduced in GitLab 14.3
/unassign @user1 @user2	 Yes	 Yes	 No	Remove specific assignees.
/unassign	 No	 Yes	 No	Remove all assignees.
/unassign_reviewer @user1 @user2 or /remove_reviewer @user1 @user2	 No	 Yes	 No	Remove specific reviewers.
/unassign_reviewer me	 No	 Yes	 No	Remove yourself as a reviewer.
/unassign_reviewer or /remove_reviewer	 No	 Yes	 No	Remove all reviewers.
/unlabel ~label1 ~label2 or /remove_label ~label1 ~label2	 Yes	 Yes	 Yes	Remove specified labels.
/unlabel or /remove_label	 Yes	 Yes	 Yes	Remove all labels.
/unlock	 Yes	 Yes	 No	Unlock the discussions.
/unsubscribe	 Yes	 Yes	 Yes	Unsubscribe from notifications.
/weight <value>	 Yes	 No	 No	Set weight. Valid options for <value> include 0, 1, 2, and so on.
/zoom <Zoom URL>	 Yes	 No	 No	Add a Zoom meeting to this issue or incident. In GitLab 15.3 and later users on GitLab Premium can add a short description when adding a Zoom link to an incident.
Work items
The following quick actions can be applied through the description field when editing work items.

Command	Task	Objective	Key Result	Action
/title <new title>	 Yes	 Yes	 Yes	Change title.
/close	 Yes	 Yes	 Yes	Close.
/reopen	 Yes	 Yes	 Yes	Reopen.
/shrug <comment>	 Yes	 Yes	 Yes	Append the comment with ¯\＿(ツ)＿/¯.
/tableflip <comment>	 Yes	 Yes	 Yes	Append the comment with (╯°□°)╯︵ ┻━┻.
/cc @user	 Yes	 Yes	 Yes	Mention a user. In GitLab 15.0 and later, this command performs no action. You can instead type CC @user or only @user. In GitLab 14.9 and earlier, mentioning a user at the start of a line creates a specific type of to-do item notification.
/assign @user1 @user2	 Yes	 Yes	 Yes	Assign one or more users.
/assign me	 Yes	 Yes	 Yes	Assign yourself.
/unassign @user1 @user2	 Yes	 Yes	 Yes	Remove specific assignees.
/unassign	 No	 Yes	 Yes	Remove all assignees.
/reassign @user1 @user2	 Yes	 Yes	 Yes	Replace current assignees with those specified.
/label ~label1 ~label2 or /labels ~label1 ~label2	 Yes	 Yes	 Yes	Add one or more labels. Label names can also start without a tilde (~), but mixed syntax is not supported.
/relabel ~label1 ~label2	 Yes	 Yes	 Yes	Replace current labels with those specified.
/unlabel ~label1 ~label2 or /remove_label ~label1 ~label2	 Yes	 Yes	 Yes	Remove specified labels.
/unlabel or /remove_label	 Yes	 Yes	 Yes	Remove all labels.
/due <date>	 Yes	 No	 Yes	Set due date. Examples of valid <date> include in 2 days, this Friday and December 31st.
/remove_due_date	 Yes	 No	 Yes	Remove due date.
/health_status <value>	 Yes	 Yes	 Yes	Set health status. Valid options for <value> are on_track, needs_attention, and at_risk.
/clear_health_status	 Yes	 Yes	 Yes	Clear health status.
/weight <value>	 Yes	 No	 No	Set weight. Valid options for <value> include 0, 1, and 2.
/clear_weight	 Yes	 No	 No	Clear weight.
Commit messages
The following quick actions are applicable for commit messages:

Command	Action
/tag v1.2.3 <message>	Tags the commit with an optional message.
 Help & feedback
Docs
Edit this page to fix an error or add an improvement in a merge request.
Create an issue to suggest an improvement to this page.
Show and post comments to review and give feedback about this page.
Product
Create an issue if there's something you don't like about this feature.
Propose functionality by submitting a feature request.
Join First Look to help shape new features.
Feature availability and product trials
View pricing to see all GitLab tiers and features, or to upgrade.
Try GitLab for free with access to all features for 30 days.
Get Help
If you didn't find what you were looking for, search the docs.
If you want help with something specific and could use community support, post on the GitLab forum.
For problems setting up or using this feature (depending on your GitLab subscription).
Sign in to GitLab.com
Twitter
Facebook
YouTube
LinkedIn
Docs Repo
About GitLab
Terms
Privacy Statement
Cookie Preferences
Contact
View page source - Edit in Web IDE Creative Commons License

On this page
Parameters
Issues, merge requests, and epics
Work items
Commit messages
Help and feedbackCC0 1.0 Universal

Statement of Purpose

The laws of most jurisdictions throughout the world automatically confer
exclusive Copyright and Related Rights (defined below) upon the creator and
subsequent owner(s) (each and all, an "owner") of an original work of
authorship and/or a database (each, a "Work").

Certain owners wish to permanently relinquish those rights to a Work for the
purpose of contributing to a commons of creative, cultural and scientific
works ("Commons") that the public can reliably and without fear of later
claims of infringement build upon, modify, incorporate in other works, reuse
and redistribute as freely as possible in any form whatsoever and for any
purposes, including without limitation commercial purposes. These owners may
contribute to the Commons to promote the ideal of a free culture and the
further production of creative, cultural and scientific works, or to gain
reputation or greater distribution for their Work in part through the use and
efforts of others.

For these and/or other purposes and motivations, and without any expectation
of additional consideration or compensation, the person associating CC0 with a
Work (the "Affirmer"), to the extent that he or she is an owner of Copyright
and Related Rights in the Work, voluntarily elects to apply CC0 to the Work
and publicly distribute the Work under its terms, with knowledge of his or her
Copyright and Related Rights in the Work and the meaning and intended legal
effect of CC0 on those rights.

1. Copyright and Related Rights. A Work made available under CC0 may be
protected by copyright and related or neighboring rights ("Copyright and
Related Rights"). Copyright and Related Rights include, but are not limited
to, the following:

  i. the right to reproduce, adapt, distribute, perform, display, communicate,
  and translate a Work;

  ii. moral rights retained by the original author(s) and/or performer(s);

  iii. publicity and privacy rights pertaining to a person's image or likeness
  depicted in a Work;

  iv. rights protecting against unfair competition in regards to a Work,
  subject to the limitations in paragraph 4(a), below;

  v. rights protecting the extraction, dissemination, use and reuse of data in
  a Work;

  vi. database rights (such as those arising under Directive 96/9/EC of the
  European Parliament and of the Council of 11 March 1996 on the legal
  protection of databases, and under any national implementation thereof,
  including any amended or successor version of such directive); and

  vii. other similar, equivalent or corresponding rights throughout the world
  based on applicable law or treaty, and any national implementations thereof.

2. Waiver. To the greatest extent permitted by, but not in contravention of,
applicable law, Affirmer hereby overtly, fully, permanently, irrevocably and
unconditionally waives, abandons, and surrenders all of Affirmer's Copyright
and Related Rights and associated claims and causes of action, whether now
known or unknown (including existing as well as future claims and causes of
action), in the Work (i) in all territories worldwide, (ii) for the maximum
duration provided by applicable law or treaty (including future time
extensions), (iii) in any current or future medium and for any number of
copies, and (iv) for any purpose whatsoever, including without limitation
commercial, advertising or promotional purposes (the "Waiver"). Affirmer makes
the Waiver for the benefit of each member of the public at large and to the
detriment of Affirmer's heirs and successors, fully intending that such Waiver
shall not be subject to revocation, rescission, cancellation, termination, or
any other legal or equitable action to disrupt the quiet enjoyment of the Work
by the public as contemplated by Affirmer's express Statement of Purpose.

3. Public License Fallback. Should any part of the Waiver for any reason be
judged legally invalid or ineffective under applicable law, then the Waiver
shall be preserved to the maximum extent permitted taking into account
Affirmer's express Statement of Purpose. In addition, to the extent the Waiver
is so judged Affirmer hereby grants to each affected person a royalty-free,
non transferable, non sublicensable, non exclusive, irrevocable and
unconditional license to exercise Affirmer's Copyright and Related Rights in
the Work (i) in all territories worldwide, (ii) for the maximum duration
provided by applicable law or treaty (including future time extensions), (iii)
in any current or future medium and for any number of copies, and (iv) for any
purpose whatsoever, including without limitation commercial, advertising or
promotional purposes (the "License"). The License shall be deemed effective as
of the date CC0 was applied by Affirmer to the Work. Should any part of the
License for any reason be judged legally invalid or ineffective under
applicable law, such partial invalidity or ineffectiveness shall not
invalidate the remainder of the License, and in such case Affirmer hereby
affirms that he or she will not (i) exercise any of his or her remaining
Copyright and Related Rights in the Work or (ii) assert any associated claims
and causes of action with respect to the Work, in either case contrary to
Affirmer's express Statement of Purpose.

4. Limitations and Disclaimers.

  a. No trademark or patent rights held by Affirmer are waived, abandoned,
  surrendered, licensed or otherwise affected by this document.

  b. Affirmer offers the Work as-is and makes no representations or warranties
  of any kind concerning the Work, express, implied, statutory or otherwise,
  including without limitation warranties of title, merchantability, fitness
  for a particular purpose, non infringement, or the absence of latent or
  other defects, accuracy, or the present or absence of errors, whether or not
  discoverable, all to the greatest extent permissible under applicable law.

  c. Affirmer disclaims responsibility for clearing rights of other persons
  that may apply to the Work or any use thereof, including without limitation
  any person's Copyright and Related Rights in the Work. Further, Affirmer
  disclaims responsibility for obtaining any necessary consents, permissions
  or other rights required for any use of the Work.

  d. Affirmer understands and acknowledges that Creative Commons is not a
  party to this document and has no duty or obligation with respect to this
  CC0 or use of the Work.

For more information, please see
<http://creativecommons.org/publicdomain/zero/1.0/>
