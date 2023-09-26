---
layout: page
title: Teams overview
description: Teams are groups of organization members that reflect your company or group's structure with cascading access permissions and mentions.
nav_order: 1
author: selkins13
---

Teams allow you to manage the permissions of multiple users in a repository or repositories at the same time. These permissions include:

- **Read:** Recommended for non-code contributors who want to view or discuss your project
- **Triage:** Recommended for contributors who need to proactively manage issues and pull requests without write access
- **Write:** Recommended for contributors who actively push to your project
- **Maintain:** Recommended for project managers who need to manage the repository without access to sensitive or destructive actions
- **Admin:** Recommended for people who need full access to the project, including sensitive and destructive actions like managing security or deleting a repository

![Organization list of teams](/assets/images/organization-administration/teams/org-list-of-teams.png)

Organization owners and team maintainers can give teams admin, read, or write access to organization repositories. Organization members can send a notification to an entire team by mentioning the team's name. Organization members can also send a notification to an entire team by requesting a review from that team. Organization members can request reviews from specific teams with read access to the repository where the pull request is opened. Teams can be designated as owners of certain types or areas of code in a CODEOWNERS file.

You can use team synchronization to automatically add and remove organization members to teams through an identity provider. For more information, see [Synchronizing a team with an identity provider group](https://docs.github.com/en/organizations/organizing-members-into-teams/synchronizing-a-team-with-an-identity-provider-group).

## Team visibility

Teams can be visible or secret:

- Visible teams can be [viewed and @mentioned](https://docs.github.com/en/articles/basic-writing-and-formatting-syntax/#mentioning-people-and-teams) by every organization member.
  
  ![Team mention](/assets/images/organization-administration/teams/team-mention.png)

- Secret teams are only visible to the people on the team and people with owner permissions. They're great for hiding teams with sensitive names or members, such as those used for working with external partners or clients. Secret teams cannot be nested under parent teams or have child teams.

## Team pages

Each team has its own page within an organization. On a team's page, you can view team members, child teams, and the team's repositories. Organization owners and team maintainers can access team settings and update the team's description and profile picture from the team's page.

Organization members can create and participate in discussions with the team.

![Team page discussions](/assets/images/organization-administration/teams/team-page-discussions-tab.png)

## Nested teams

You can reflect your group or company's hierarchy within your GitHub organization with multiple levels of nested teams. A parent team can have multiple child teams, while each child team only has one parent team. You cannot nest secret teams.

Child teams inherit the parent's access permissions, simplifying permissions management for large groups. Members of child teams also receive notifications when the parent team is @mentioned, simplifying communication with multiple groups of people.

For example, if your team structure is Employees > Engineering > Application Engineering > Identity, granting Engineering write access to a repository means Application Engineering and Identity also get that access. If you @mention the Identity Team or any team at the bottom of the organization hierarchy, they're the only ones who will receive a notification.

![Nested teams example](/assets/images/organization-administration/teams/nested-teams-eng-example.png)

To easily understand who shares a parent team's permissions and mentions, you can see all of the members of a parent team's child teams on the Members tab of the parent team's page. Members of a child team are not direct members of the parent team.

![Team and subteam members](/assets/images/organization-administration/teams/team-and-subteam-members.png)

You can choose a parent when you create the team, or you can move a team in your organization's hierarchy later.

## References

- [About teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams)
- [Team discussions](https://docs.github.com/en/organizations/collaborating-with-your-team/about-team-discussions)
- [Creating a team](https://docs.github.com/en/organizations/organizing-members-into-teams/creating-a-team)
- [Adding members to a team](https://docs.github.com/en/organizations/organizing-members-into-teams/adding-organization-members-to-a-team)
- [Managing code review assignment](https://docs.github.com/en/organizations/organizing-members-into-teams/managing-code-review-assignment-for-your-team)
- [Synchronizing a team with IdP group](https://docs.github.com/en/organizations/organizing-members-into-teams/synchronizing-a-team-with-an-identity-provider-group)
