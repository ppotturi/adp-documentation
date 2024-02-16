---
title: How to create a platform service
summary: How to create a platform service on to ADP.
authors:
    - Logan Talbot
date: 2024-02-15
weight: 1
---
# How to create a platform service

In this how to guide you will learn how to create a service on to ADP within your delivery project. You will also learn what automated actions that will take place.

## Prerequisites

Before onboarding a delivery project ou will first need to ensure that:

- [Onboarded delivery project on to ADP](../1.-Getting-Started/onboarding-a-delivery-project.md).
- Active user on the ADP Portal with admin permissions for the delivery project on the ADP portal.

## Overview

By completing this guide you will have completed these actions:

- If GitHub team for the services' delivery project is not present it will create a new GitHub team.
- Creates team repository in Defra GitHub Org and added to the delivery project's GitHub team.
- Scaffolds a application in your selected language and defines optional infrastructure.
- Scaffolding of ADO project if not already done.
  - Share service connection and agent pools with ADO project.
  - Create ADO environment and variable group in ADO project.
- Creation of ADO pipeline for the CI/CD for service in selected ADO project/ location.
- Authorizes service connection between new created ADO Pipeline & GitHub repository.
- Starts the running of ADO pipeline. Build application and SND3 without approval.
  - Init Sonar Cloud, Snyk, etc.
- Register in Backstage catalog (via catalog info file).

# Guide
