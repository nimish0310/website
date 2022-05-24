---
layout: default
title: Use cases
nav_order: 2
---

# Use cases
{: .no_toc }


## Table of contents
{: .no_toc .text-delta }
1. TOC
{:toc}

## Sensitive data classification and auditing for GDPR and CCPA
Given a set of predefined meta data for identifying sensitive data such PII for GDPR and PII, DataSage can both identify and track sensitive data across enterprise data sources as it moves across various databases (which are tracked by DataSage of course).

## Compliance reporting
Given a set of predefined compliance reports around data access, audit and permissions, DataSage can report back on compliance templates such as GDPR, CCPA etc.

## Identifying sensitive data in non senstiive targets
In many cases where data is shared with third party contractors etc., data obsfucation and differential privacuy is expected but not always implemented. DataSage can be used to track sensitive data sources including specific fields, or a group of fields into newer non sensitive targets.

 
## Tracking application users who access sensitive data
Datasage can be used to track sensitive data access by individual application users through the use of network policies that can track inbound connections as well as the user ids that the jwt token represents while accessing the database.

## Data lineage 
Datasage can help build data lineage graphs of all access to sensitive data.

## Data provenance of S3 databases
Datasage can be used to track data provenance of sensitive data in container environments as it moves through workloads and exits the network. This feature is currently only available for S3 databases.

 