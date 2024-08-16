---
title: Onboarding a delivery project
summary: Onboard a delivery project on to ADP.
uri: https://defra.github.io/adp-documentation/Getting-Started/onboarding-a-delivery-project/
authors:
    - Logan Talbot
    - Lorenzo Squillante
    - Danny May
date: 2024-08-15
weight: 2
---

# Onboarding a delivery project

This getting started guide summarises the steps for onboarding a delivery project onto ADP via the Portal. It also provides an overview of the automated processes involved.

## Prerequisites

Before onboarding a delivery project you will first need to ensure that:

- The delivery programme for your project has been onboarded onto ADP, see the Getting Started guide for [Onboarding a delivery programme on to ADP](onboarding-a-delivery-programme.md).
- You have an active user account within the ADP Portal with admin permissions to create a delivery project within your selected delivery programme.
- You have a "Service Code" and "Cost Centre" for your delivery project.

## Overview

By completing this guide you will have completed these actions:

- [X] Adding a new delivery project to ADP portal database under your programme.
- [X] Assign delivery project admins to adminster delivery project.
- [X] Creation of a new ADO Team on a selected ADO project.
- [X] Creation of new GitHub Teams for the delivery project.
- [X] Adding Azure group(s) for the delivery project's tech users. Members of this group will be given access to common platform resources and project resource group in tenants, and Defra
  - [X] O365_DefraDev  - SND3, data and control plane read/ write.
  - [X] Defra - DEV1, TST1/2, data and control plane read/ write.
  - [X] Defra - PRE1, PRD1, ready access on the control plane. No data plane access given

# Guide

## Creating a Delivery Project

Once you have navigated to the 'ADP Data' page you will be presented with the 'Delivery Projects' option. 
![ADP Data](../images/adp-data.png)
By clicking 'View' you will have the ability to view existing Delivery Projects and add new ones if you have the admin permissions. 
![View Delivery Projects](../images/adp-view-delivery-project.png)

## Entering Delivery Project information

You can start entering Delivery Projects information by clicking the 'Add Delivery Projects' button.
![Add Delivery Projects](../images/adp-create-delivery-project.png)
You will be presented with various fields; some are optional. For example, the 'Alias', 'Website', 'Finance Code' and 'ADO Project' are not required, and you can add them later if you wish.

If the Delivery Programme for your project has already been created and you are an admin for it, it will appear in the Delivery Programme dropdown, and you will be able to select it accordingly. 

This form includes validation. Once you have completed inputting the Delivery Project Information and pressed 'create', the validation will run to check if any changes need to be made to your inputs.

Once the project is created, the Github Teams will automatically be created. There will be one team for users who are Technical Team Members of the project, and one for users who are both a Technical Team Member and Admin of the project.

Your newly created Delivery Project will now show up in the table, and also in the Catalog as a new Group. You can edit the project by clicking the edit button, or view the project in the catalog by clicking the link in the Name column.

## Updating Delivery Project information
Once you have created your Delivery Project, you will automatically be redirected to the view page which will allow you to look through existing projects and edit them. 
![Update Delivery Projects](../images/adp-view-edit-delivery-project.png)

### Manage delivery project members.

Members of a delivery project are able to be managed through the Delivery Projects catalog page, under the Manage Members tab. You can easily access this page by clicking the user config button.

![Edit Delivery Project Members](../images/adp-edit-delivery-project-members.png)

When adding a new user to the project, you must select the role you wish to give to them. If you give them the Technical Team Member role, you will also need to supply their github username as they will be added to the relevant teams in github, giving them access to any repositories scaffolded for this Delivery Project.

### Adding creation of a new ADO Team on a selected ADO project.
...
### Adding Azure group(s) for the delivery project's tech users.
...