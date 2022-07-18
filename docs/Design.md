---
layout: default
title: Design
nav_order: 2
---

# DataSage design
{: .no_toc }


## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

![Stack](/assets/images/Architecture.png)


Datasage works by talking to the database audit mechanisms so that data can be collected and audited in the least disruptive manner. Certain policies (such as protection of allow / deny) also initiate database changes in terms of grant statements to allow or deny specific actions against the database.
