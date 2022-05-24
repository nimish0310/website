---
layout: default
title: FAQs
nav_order: 7
---

# Frequently asked questions
{: .no_toc }


## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## What are all the databases that DataSage Works with?

Datasage works well with MySQL Percona ExtraDB Cluster (PXC), Postgres, S3 and has upcoming support for MSSQL Server

## Does Datasage require changes to my application?

No. Datasage does not require any changes to your application code, database drivers or anything that changes the nature of the application in anyway.

## What are the prerequisites for Datasage installation.

The most important prerequisite (which is mostly already enabled in places where sensitive data exists) is that database audit logs are enabled.

Information for <a href="https://www.percona.com/doc/percona-server/8.0/management/audit_log_plugin.html"> Percona </a> and <a href="#"> PostgresSQL </a> are given as links. 

## What is a Sensitive Class?

A sensitive data is any definition available in the form of metadata. DataSage provides several sensitive data definitions out of the box called as Sensitive Classes

Sensitive classes have a 1:1 with a type of data

- Password
- email id
- Phone number
- Address
- Credit card number


All of these fields (regardless of the type defintition can be called as a Sensitive class)

## What is a sensitive tag

Groups of sensitive classes that represent a compliance standard such as CCPA is termed as a sensitive tag.

## Does Datasage come with sensitive data configured to be tracked out of the box?

Datasage has dozens of sensitive classes, sensitive tags and data security controls out of the box that enables you to start auditing your data immediately.


 

