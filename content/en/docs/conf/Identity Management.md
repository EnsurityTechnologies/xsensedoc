---
title: "Identity Management"
description: " "
lead: ""
date: 2020-11-12T15:22:20+01:00
lastmod: 2020-11-12T15:22:20+01:00
draft: false
images: []
weight: 710
toc: true
---

Roles, users, organization units and their permissions are managed under the Identity Management section. Under the Identity management tab, there are three sub sections

- Organization Unit
- Roles
- Uses

From the uses tab, the list of users and their corresponding roles and user attributes can be viewed. You can add, modify, and remove users as well as give them roles. The menu items and associated features have permission. This means that in order to make them visible, the current user must possess the necessary rights. These capabilities are already available to users with the admin role (including the admin user). Open the Permissions dialogue on the Roles or Users page and check the permissions if you want to enable permissions for additional roles or users

## Organization Units (OU)

Users, groups, and computers can all be stored under an Organization Unit here after referred as 'OU', which is a container found within an XSense IdP server. The smallest unit to which a Group Policy setting or account authorization can be applied is known as a subunit. Multiple OUs may exist within an AD organisational unit, but each of the OU's constituent attributes must be distinct.

### OU Creation

This descibes the process of creating a new OU and adding the members, assigning the roles to newly created OU.

- Navigate to the Organisation Unit, which is under Identity Management, to start a new Organisation Unit. Select **Add root unit**.
- Enter the name of the organisation unit and click on **Save**.

#### Add Member

Once the OU is created, the admin can add members by clicking on the OU name, and click on **Add Member** on the right side under the Members tab.
After choosing the requried members click on **Save**.

#### Add Role

After the desired users are selected and added to the OU, the admin can assing a role by clicking on the **Roles** tab. Click on **Add Role** and choose the required role for the OU.

#### Additional Options

- On the available OU, the admin can perform the multiple operations
  - **Edit**: Allows the admin to edit the name of the Organisation Unit.
  - **Add Sub-unit**: Allows the administrator to create a sub unit for more accurate user categorisation. Provides the admin the ability to add a sub-organizational unit. Each subunit can have an individual role.
  - **Add Member**: Allows the admin to add users to the organisation unit.  
  - **Add Role**: Assign the organisation unit the permissions. The Roles created under the Roles section are where these permissions are selected.
  - **Delete**: Delete the organisation unit, but doing so does not remove the associated users, roles or computers from the XSense IdP portal.

## Roles

Roles are used for defining the access rights and permissions for a user to perform a specific operation. By default, the application provides two roles, one is the Admin role and the other is the User role. The admin can choose any role for the user during the user creation. The admin can also create new roles and assign these roles to users. The Admin can configure the permissions based on the role created. XSense IdP provides two default roles.

- **Admin**:  The users assigned to this role are administrators and have all the permissions in the application. These users can access the dashboard and manage the users, applications, AMS, Devices, and Settings and make any necessary changes to the application.

- **User**: The users assigned to this role will not have any access to the dashboard. If required, the admin can modify the permissions for this user role from Actions>> Permissions and choose the necessary permissions.

### Role Creation

- To create a new role, click on **Create new role** enter the **Role Name** and click on **Save**. The administrator can decide whether the newly created role will be a default role or a public role during the role creation process. All newly imported users will be assigned to this position if the admin designates it as the default role.
- Once the role is created, there are multiple actions that can be performed on a role by clicking on **Action** button aganist the role. The options that are avialable under Actions are listed below:
  
  - **Edit**: Permits the administrator to change the role's name and whether it is default or public.
  - **Claims**: Currently, this option is being implemented.
  - **Permissions**: The selected permissions will be enforced for the role, and the users assigned to that role will inherit these permissions.
  - **Change History**: Provides a record or log of alterations, modifications, or updates made to the particular role.
  - **Delete**: Removes the role from the XSense IdP portal.

## User

Users are verified by XSense IdP using either an external directory service or the internal XSense User Directory. You can add, change, and delete user accounts for applications or mobile device management by using directory service functionalities. As an alternative to or in addition to using the XSense IdP user directory, you can also set up a connection to an existing external directory service. The XSense IdP server supports a number of directory services that allow for user onboarding. The directory services that are offered are:

- On-Prem Active Directory
- Azure AD
- Manual - XSense IdP user store

Different responsibilities can be assigned to users once they have been onboarded to the XSense IdP server. Permissions for each user can also be modified on the XSense IdP server.


| User Attributes @ Local / Hybrid AD | User Attributes @ Azure AD |
|---|---|
| userPrincipalName  | id  |
|  sAMAccoutnName | userPrincipalName |
|  cn | display name  | 
|given name | given name|
| display name | last name |
|email | email|

### XSense IdP local directory

When adding the user manually, the admin can choose the type of role that will be assigned to the user. These users are stored locally on the XSense IdP server. These users won't have their data synchronized with any enterprise user store directory, such as on-premises AD, Azure AD, etc. The altered permissions won't be synchronized with the organization user store.

- To add the User, navigate to Users under Identity Management. Click on **New User**.
- In the pop-up form for the new user creation, fill in the mandatory field and choose the necessary role for the user. The default Role is User; however, the admin can choose any other Role available.
- Click on **Save** to create the user.

### User Import from configured directory services

Users can be on-boarded to XSense IdP server from connected LDAP server. The users can only be onboarded by administrators or users with administrator privilege authority. The "Users" role allocated users can have any of the available MFA choices in XSense IdP server.

- To initiate the import, navigate to the **Users** section under Identity Management. Click on **Import Users**.
- In the popup windows, based on the directory service configured in **Settings** choose the directory service and click on **Import Users**.
- Choose the users and click on **Sync**. The selected users will be imported to XSense IdP server.
- The synced user role can be modified by clicking on **Actions** and **Edit**. Choose the necessary role for the user and click on **Save**.
- The user details modified under the User information section do not get updated in the AD including the permissions. The modifications are local to the XSense IdP Server.
