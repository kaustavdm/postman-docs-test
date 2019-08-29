---
title: Roles and permissions
page_id: roles_and_permissions
warning: false
---

# roles and permissions

Roles and permissions in Postman have been enhanced to provide a more robust access-control mechanism. In Postman v7, you access features through assigned roles that have their own set of user permissions.

This chapter describes the following topics:

* [Understanding roles in Postman](roles_and_permissions.md#understanding-roles-in-postman)
* [List of roles and permissions](roles_and_permissions.md#list-of-roles-and-permissions)
* [Roles before and after](roles_and_permissions.md#roles-before-and-after)
* [Migrating to Postman v7](roles_and_permissions.md#migrating-to-postman-v7)

## Understanding roles in Postman

Permissions to perform certain tasks and/or operations are assigned to specific roles in Postman. For instance, Postman provides an admin-level role to help manage the permissions of Postman for the entire team. Likewise, Postman has other roles with specific permissions.

The diagram below illustrates the roles in Postman:

[![roles overview](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/RBAC3.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/RBAC3.png)

The following is a brief outline of the main roles:

* **Collection viewer** can view, run, and share a collection. When a viewer shares a collection it carries the same viewer permissions to the viewer with whom it is shared. 
* **Collection editor** can manage a collection and controls the highest level administrative and security settings.
* **Workspace collaborator** can view all resources in the workspace, has add and remove privileges, can create history, and even add members.
* **Workspace admin** can edit workspace’s information like name, summary, settings, remove members and change workspace roles, and delete the workspace.
* **Team developer** can access some team resources \(collections, environments, workspaces\).
* **Team admin** can’t access team resources, can edit team details, settings and invite/remove team members.
* **Team billing** can’t access team resources, can access billing related things.

## List of roles and permissions

Roles and permissions is not a new feature in Postman. In Postman v7 the roles have been enhanced to provide a fine-grained access management of its features. This sections clearly outlines the roles and permissions for collections, workspaces, and teams in a table format.

This section describes the following topics:

* [Collection roles](roles_and_permissions.md#collection-roles)
* [Workspace roles](roles_and_permissions.md#workspace-roles)
* [Team roles](roles_and_permissions.md#team-roles)

### Collection roles

In Postman v7, collections have two roles - **Collection Viewer** and **Collection Editor**. The following table illustrates the roles and permissions of collections:

| Collections | Viewer | Editor |
| :--- | :--- | :--- |
| Add, edit, and delete mock servers |  | ☑ |
| Add, edit, and delete monitors |  | ☑ |
| Edit and delete a collection |  | ☑ |
| Manage roles on collections |  | ☑ |
| View and run collections |  | ☑ |
| View and run collection runs | ☑ | ☑ |
| Export a collection | ☑ | ☑ |
| Fork a collection | ☑ | ☑ |
| Merge forks on a collection | ☑ | ☑ |
| Publish collection documentation and add to API Network or Postman template |  | ☑ |
| Share collection to a different workspace |  | ☑ |
| Tag and restore collection versions |  | ☑ |

### Workspace roles

In Postman v7, workspaces have two roles - **Workspace Collaborator** and **Workspace Admin**. The following table illustrates the roles and permissions of workspaces:

| Workspaces | Collaborator | Admin |
| :--- | :--- | :--- |
| Add and remove collections, environments | ☑ | ☑ |
| View, create, edit, and delete Collection runs, Header Presets, History, and Integrations | ☑ | ☑ |
| Delete workspace |  | ☑ |
| Join and leave workspace | ☑ | ☑ |
| Add mock servers and monitors | ☑ | ☑ |
| View workspace contents and data like name, summary, and settings | ☑ | ☑ |
| Edit workspace details like - name, summary, and settings |  | ☑ |
| Add members | ☑ | ☑ |
| Remove members |  | ☑ |
| Manage roles and visibility of the workspace |  | ☑ |

### Team roles

In Postman v7, teams have three roles - **Developer**, **Admin**, and **Billing**. The following table illustrates team's roles and permissions:

| Teams | Developer | Admin | Billing |
| :--- | :--- | :--- | :--- |
| Create and delete invitations |  | ☑ |  |
| Edit team information and logo |  | ☑ |  |
| Manage team roles \(except billing\) |  | ☑ |  |
| Remove users from the team |  | ☑ |  |
| Manage custom domains |  | ☑ |  |
| Manage authentication methods |  | ☑ |  |
| View monitoring usage data for all monitors created by the team |  | ☑ |  |
| View team audit logs |  | ☑ |  |
| Create and manage payment links |  | ☑ | ☑ |
| Use a purchase key |  | ☑ | ☑ |
| View all published collections in the team | ☑ | ☑ |  |
| Manage billing details |  | ☑ |  |
| Manage payment and payment methods |  | ☑ |  |
| Cancel and change team plan |  | ☑ | ☑ |
| Assign billing role |  | ☑ | ☑ |
| View collections, environments, mock servers and monitors visible to the team |  | ☑ | ☑ |
| View and create team workspaces |  | ☑ | ☑ |
| View team activity feed |  | ☑ | ☑ |
| View team's custom domains and use them to publish documentation |  | ☑ | ☑ |

## Roles before and after

A user's role determines what they can and cannot do in Postman. Each role has a default set of permissions. The following section illustrates the roles prior to version 7 and post 7. The following lists the old roles and the newer ones feature-wise:

* Collections
  * _Can view_ changed to **Collection Viewer**
  * _Can edit_ changed to **Collection Editor**
* Workspace \(No roles existed prior to version 7.0\)
  * Workspace Collaborator
  * Workspace Admin
* Team

  * _User_ changed to **Developer**
  * Admin 
  * Billing

  **Note:** In the Postman app UI, the right-click option _Modify team permissions_ has changed to **Manage Roles**. Also note that the older set of roles applied till Postman app version 6.

## Migrating to Postman v7

To know more about migration-related information, please refer to [migrating to v7](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman_pro/managing_postman_pro/migrating_to_v7/README.md) section.

