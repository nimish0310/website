---
layout: default
title: FAQs
nav_order: 6
---

# Frequently Asked Questions
{: .no_toc }


## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## What are all the Databases that DataSage Works with?

DataSage works well with MySQL Percona ExtraDB Cluster (PXC), Postgres, S3 and has upcoming support for MSSQL Server.

## Does DataSage require changes to my application?

No. Datasage does not require any changes to your application code, database drivers or anything that changes the nature of the application in anyway.

## What are the prerequisites for DataSage Installation.

The most important prerequisite _(which is mostly already enabled in places where sensitive data exists)_ is that database audit logs are enabled.

Information for <a href="https://www.percona.com/doc/percona-server/8.0/management/audit_log_plugin.html"> Percona </a> and <a href="#"> PostgresSQL </a> are given as links. 

## What is a Sensitive Class?

A sensitive data is any definition available in the form of metadata. DataSage provides several sensitive data definitions out of the box called as Sensitive Classes

Sensitive classes have a 1:1 with a type of data:

- Password
- email id
- Phone number
- Address
- Credit card number


All of these fields _(regardless of the type defintition can be called as a Sensitive Class)_.

## What is a Sensitive Tag?

Groups of sensitive classes that represent a compliance standard such as CCPA is termed as a Sensitive Tag.

## Does DataSage come with sensitive data configured to be tracked out of the box?

Datasage has dozens of sensitive classes, sensitive tags and data security controls out of the box that enables you to start auditing your data immediately.
