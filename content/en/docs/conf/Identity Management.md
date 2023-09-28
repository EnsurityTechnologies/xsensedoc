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

From the uses tab, the list of users and their corresponding roles and user attributes can be viewed. You can add, modify, and remove users as well as give them roles. The menu items and associated pages have permission. This means that in order to make them visible, the current user must possess the necessary rights. These capabilities are already available to users with the admin role (including the admin user). .Open the Permissions dialogue on the Roles or Users page and check the permissions if you want to enable permissions for additional roles or users

## Organization Units (OU)

Users, groups, and computers can all be stored under an Organization Unit here after referred as 'OU', which is a container found within an XSense IdP server. The smallest unit to which a Group Policy setting or account authorization can be applied is known as a subunit. Multiple OUs may exist within an AD organisational unit, but each of the OU's constituent attributes must be distinct.

  ![ou](images/ou.png)

### New OU creation

This descibes the process of creating a new OU and adding the members, assigning the roles to newly created OU.

- Navigate to the Organisation Unit, which is under Identity Management, to start a new Organisation Unit. Select **Add root unit**.

  ![newou](images/newou.png)

- Enter the name of the organisation unit and click on **Save**.

#### Add Member

Once the OU is created, the admin can add members by clicking on the OU name, and click on 'Add Member' on the right side under the Members tab.

  ![OUMember](images/OU_addMember.png)

- After choosing the requried members click on 'Save'.

#### Add Role

- After the desired users are selected and added to the OU, the admin can assing a role by clicking on the "Roles" tab. Click on Add Role and choose the required role for the OU.

  ![OUMember](images/OU_addRole.png)

#### Additional Options

- On the available OU, the admin can perform the multiple operations

  ![OU dropdown options](images/OUdropdownoptions.png)

  - **Edit**: Allows the admin to edit the name of the Organisation Unit.
  - **Add Sub-unit**: Allows the administrator to create a sub unit for more accurate user categorisation. Provides the admin the ability to add a sub-organizational unit. Each subunit can have an individual role.
  - **Add Member**: Allows the admin to add users to the organisation unit.  
  - **Add Role**: Assign the organisation unit the permissions. The Roles created under the Roles section are where these permissions are selected.
  - **Delete**: Delete the organisation unit, but doing so does not remove the associated users or roles from the server.

## Roles

Roles are used for defining the access rights and permissions for a user to perform a specific operation. By default, the application provides two roles, one is the Admin role and the other is the User role. The admin can choose any role for the user during the user creation. The admin can also create new roles and assign these roles to users. The Admin can configure the permissions based on the role created. XSense IdP provides two default roles.

- **Admin** :  The users assigned to this role are administrators and have all the permissions in the application. These users can access the dashboard and manage the users, applications, AMS, Devices, and Settings and make any necessary changes to the application.

- **User** : The users assigned to this role will not have any access to the dashboard. If required, the admin can modify the permissions for this user role from Actions>> Permissions and choose the necessary permissions.

### Role Creation

- To create a new role, click on “Create new role” enter the Role name and assign the required permissions. During the role creation, the admin can choose the default role for all the new users.

  ![rolecreation](images/rolecreation.png)

- Once the role is created, click on Actions, and choose “Permissions.” In the pop up choose the necessary permissions required and click on Save.

  ![permissions](images/permissions.png)

- The chosen permissions will be applied to the role. The users assigned to the role will have the assigned permissions only.

## User

XSense IdP server supports various directory serivces using which the users can be onboarded. The available directory services are:

- Azure AD
- LDAP
- Manual

Once the uses are onboarded to XSense IdP server, different roles can be assigned to the user. Also, in XSense IdP server, permissions for each users can also be managed.

### Creating users Manually

When adding the user manually, the admin can choose the type of role that will be assigned to the user.

- To add the User, navigate to Users under Identity Management. Click on New User.
- In the pop-up form for the new user creation, fill in the mandatory field and choose the necessary role for the user. The default Role is User; however, the admin can choose any other Role. Available.
- Click on Save to create the user.

### Importing Users from Local AD

Users can be onboarded to XSense IdP server from connected LDAP server. The users can only be onboarded by administrators or users with administrator privilege authority. The "Users" role allocated users can have any of the available MFA choices in XSense IdP server.

- To initiate the import, navigate to the Users section under Identity Management. Click on Import Users.
- In the popup windows, click on Import Users under the LDAP section.

  ![permissions](images/permissions.png)

- Choose the users and click on Sync. The selected users will be imported to XSense IdP server.

  ![users](images/users.png)

- The synced user role can be modified by clicking on Actions and Edit. Choose the necessary role for the user and click on Save.
- The user details modified under the User information section do not get updated in the AD including the permissions. The modifications are local to the XSense IdP Server.

### Importing Users from Azure AD

* Need to add content

### Importing users from GCP

* Need to add content
