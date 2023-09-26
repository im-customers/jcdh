---
layout: page 
title: Teams best practices 
description: Describes the best practices and recommendations while using teams in your organization 
nav_order: 1
author: selkins13
toc: true
---

The concept of `Teams` in GitHub allows for greater flexibility for collaboration and integration, as well as separation
of repositories and permissions. With _nested teams_ we can create a hierarchy for our applications, create communities
of practice, invoke logical groupings of functional areas, as well as manage our teams of people effectively. If we take
a step back and look at `Teams` as being more than simply HR groupings of people we can see many ways to effectively
organize our software.

### Uses for `Teams`

- Teams can be used to logically separate `Product Families`
- Teams can be used to logically separate `Products`
- Teams can be used to logically correlate areas of expertise
- Teams can be used to logically correlate `Product Features`
- Teams can be used to logically group areas of responsibility
- Teams can be nested, which provides logical groupings for these teams' areas of ownership
- Teams can be used to logically represent Departments

### Organization and permissions

To understand more about teams and permissions reference the following.
<iframe src="/assets/pdf/teams-and-permissions.pdf" width="100%" height="600px"></iframe>

You can also find a good reference of best practices within your organization
in [this community post](https://github.community/t/best-practices-for-organizations/10205).

### Product and People teams

![interest-groups](/assets/images/organization-administration/teams/interest-groups.png)

We have a `Product Family Team` underneath that Org. Within that `Product Family Team`, we can have
multiple `Product Teams`. We want to make sure that people working on the `Product A` are able to see only the
repositories belonging to it.

If we have all 3 `Products` (`Product-A`, `Product-B` and `Product-C`) created as `Teams`, and have each of these
`Teams` as a children of the `Product Family Team`, then we can see all repos from the `Product Family` or just the
repos belonging to the `Product` in the teams view (`https://github.com/orgs/:org/teams/:teamName/repositories`). We can
add then these teams to the repositories for them to get access.

Once we have logically organized our `Product Family` and `Product Teams`, we can organize our developers
with `People Teams`, and add those `People Teams` into the repositories as necessary. In the image, some people
from `devGroupA` also belong to `org/SQL` and `org/security` and each of those groups can be added to repositories as
needed to provide the right access.

In the image below, we see that we have `Client Apps` as the `Product Family` and Atom as the `Product`. The only
repositories visible from this Team view are those that belong to Atom product team.

![github-teams-8](/assets/images/organization-administration/teams/product-teams.png)

### How to configure the structure

- Plan the product families and product teams that you want to have
- Plan the developer teams that you want to have
- You can go to [https://github.com/orgs/:org/teams](https://github.com/orgs/:org/teams) and:
  - Create the Product families
  - Create the Product teams and assign their parent as the corresponding Product family
  - Add the Product teams access to the repositories they need to have access to
  - Create an Everyone team. This team is useful for wide company announcements without hosting a webinar to explain something. Try not to abuse this `@all` pings.
  - Create the People teams and assign the parent as Everyone
  - Add the People teams to the repositories as needed

> ⚠️ To add teams as children of other teams they cannot be secret teams.

### Team interests

Additionally you can create teams for interests/technology in order to help with PR review processes or issue
discussions (javascript, go, data science...). People should join this teams by own interest to help on certain projects
if they get the request.

Creating a process within the company to create new `team interests` teams is recommended.

### Team sync enablement

If you use a SAML provider that
supports [team synchronization](https://help.github.com/en/github/setting-up-and-managing-organizations-and-teams/synchronizing-teams-between-your-identity-provider-and-github)
, you may want to enable it for the `People teams` and not for the `Product` teams. Team sync can only be enabled on
leafs (groups with no children teams), so people teams are the best option.

You can make the `People` teams structure match your SAML provider structure if needed and then make the parents as
logical structures.
