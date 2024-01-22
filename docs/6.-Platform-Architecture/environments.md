# Environments

## Overview
The table below details the environments the Platform supports, there purposes, and whether they're mandatory for going live / on the RTL path.

* All environments for Platform services reside within the Defra tenant, unless otherwise specified.
* 1-1 mapping between Services Environment  & Azure Subscription
* The number at the end of the environment code designates the Subscription/Environment number.

| **Shared Services Environment** | **Use case** | **Route-to-live** | **Environment Code/Subscription** | **Additional Information** |
|--|--|--|--|--|
| Production | Live Services, Public & Private beta. | Yes | PRD1 | |
| Pre-Production | Automated Acceptance testing prior to production. | Yes | PRE1 |VPN Required. |
| Demo/Test | External demonstrations, PEN tests etc. | No | TST2 | VPN Required. |
| Test | General testing, performance testing, exploratory testing | No | TST1 | Intended for demo's to external and internal stakeholders |
| Development | Pre-merge automated tests, Pull Request checks etc. | Yes | DEV1 | VPN Required. |
| Sandpit | Testing infrastructure changes, proof of concepts, experimentations | No | SND1, SND2, SND3 |Tenant: 0365_DefraDev. VPN Required. |
| Shared Services 3| Management and Shared Services - Test and all environments below. POC/development area.| No | SSV3| Tenant: 0365_DefraDev |
| Shared Services 5| Management and Shared Tests - Production and all environments below. Live services. | No | SSV5| Contains live ACR. |

**The Subscriptions that map to the environments [documentation can be found here.](???)**

## Route to live overview

For all Service teams, the defined minimum 'route to live' path is:

- Dev > Pre-Prod > Production (Live). 
-- _All other environments are optional: SND, TST, DMO_


This means that Service Teams must have passed automated checks/smoke tests in the Pre-prod environment and any initial merge and validation checks in Development only before going Live. All other environments are there on-demand for teams. We may have additional environments if the future if needed, such as a dedicated ITHC/PEN Test area, but again these would be optional.
