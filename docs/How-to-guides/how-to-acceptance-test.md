---
title: How to acceptance test
summary: How to create and run acceptance test for a service
uri: https://defra.github.io/adp-documentation/How-to-guides/how-to-acceptance-test/
authors:
  - Rajesh Venkatraman
date: 2024-07-17
weight: 2
---

## How to acceptance test

In this how to guide you will learn how to create, deploy, and run acceptace test for a Platform service (Web App, User Interface etc) for your team.

## Prerequisites

Before adding acceptance tests for your service, you will need to ensure that:

- [Onboarded delivery project on to ADP](../Getting-Started/onboarding-a-delivery-project.md)
- [Created a Platform Service for your team/delivery project](../How-to-guides/how-to-create-a-platform-service.md)

## Overview

By completing this guide, you will have completed these actions:

- [x] Learned how to add acceptance test for your service.
- [X] Learned how to run acceptance test locally.
- [X] How to customize your pipeline to run acceptace tests based on tags for different env.

## Guide

### How to add acceptance test for your service?

You may add tags for features and scenarios. There is no restrictions on the name of the tag. Recommended tags @sanity @smoke @regression
[refer](https://github.com/DEFRA/ffc-demo-web/blob/main/test/acceptance/features/subsidenceStartDate.feature)

If custom tags are defined then the pipeline need to be customized to run those tests as detailed in following sections.

### How to run acceptance test locally?

1. Set required tags, default is empty string which will run all tests.

- pwsh : `$ENV:TEST_TAGS = "@sanity or @smoke"`
- shell: `export TEST_TAGS = "@sanity or @smoke"`

2. Run the acceptance test script under scripts folder within the repo.

### How to customize your pipeline to run acceptace tests?

Every pipeline run includes steps to run varoious tests pre deployment and post deployment.
These tests may include unit, integration, acceptance, performance, accessibilty etc as long as they are defined for the service.

You can customize the tags and environments where you would like to run specific features or scenarios of acceptance test

```yaml
postDeployTest:      
  testEnvs:
    performanceTests: snd4, pre1
    accessibilityTests: snd4, tst1,     
    acceptanceTests:
      - env: snd4
        tags: '@demotag'
      - env: dev1
        tags: '@sanity or @smoke'
  envToTest: snd4,dev1,tst1,pre1
```

if not defined, the pipeline will run with following default settings

```yaml
postDeployTest:      
  testEnvs:
    performanceTests: snd4, pre1
    accessibilityTests: snd4, dev1, tst1    
    acceptanceTests:
      - env: snd4
        tags: '@sanity or @smoke'
      - env: dev1
        tags: '@smoke'
      - env: tst1
        tags: '@smoke or @regression'         
  envToTest: snd4,dev1,tst1,pre1
```

Please refer ffc-demo-web pipeline: [Refer](https://github.com/DEFRA/ffc-demo-web/blob/main/.azuredevops/build.yaml)

Test execution reports will be available via Azure DevOps Pipelines user interface for your project and service.
