---
layout: default
title: Getting Started
nav_order: 4
---

# Getting Started with DataSage
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Installing DataSage
> System prerequisite - Linux Operating System

Get installation script:
```sh
cd /tmp && curl -sfL https://raw.githubusercontent.com/datasage-io/datasage/main/install.sh -O install.sh
```
Give execute permission for file installscript.sh
```sh
chmod +x install.sh
```
Execute as below 
```sh
./install.sh
```
Start the Datasage server as below:
```sh
datasage 2>@1 &
```
You will see message *"gRPC server on 8089 port started"*

## 2. Install DataSage-CLI application
Go to a <ins>/tmp</ins> directory or any working Linux System

Download DataSage-CLI Binary from github as below:
```sh
curl -L -o datasage-cli.tar.gz 
https://github.com/datasage-io/datasage-cli/releases/download/0.1.0/datasage-cli_0.1.0_linux_amd64.tar.gz
```
Unzip the downloaded file as below:
```sh
gunzip datasage-cli.tar.gz
```
Untar the file as below:
```sh
tar -xvf datasage-cli.tar
```
File datasage-cli will be found in the directory 
<ins>./datasage-cli</ins>
Issue command as below:
```sh
./datasage-cli datasource list
```
- When you get response as "No Data" it indicates that no datasource is found
>Installation is complete now

## How to add a DataSource (MySQL)
```sh
./datasage-cli datasource add --name <nameOfDataSource> --description <descriptionOfDatabase> --type mysql --version 8 --host <dbhostname> --port <portnumber> --user <user> --password <password> 
```
- Example
When one have a MySQl DB running with following information  
        host: localhost
        port: 3306
        user: root
        password: 'Accuknox@123'
Invoke datasource add command with following input:
```sh
./datasage-cli datasource add --name Org1Analytics --description "Org1 production data scanning with datasage" --type mysql --version 8 --host localhost --port 3306 --user user1 --password  user1dbpassword --datadomain prod 
```
Wait for few secconds... Command will reponse as below:
"Data Source added for Scanning"

### How to list the Datasources configured in DataSage
Invoke command as below:
```sh
./datasage-cli datasource list
```
> Reponse will be as below:

| ID | DATA DOMAIN |      NAME     |                 DESCRIPTION                 | TYPE  | VERSION |
|----|-------------|:-------------:|:-------------------------------------------:|-------|---------|
| 1  |     prod    | Org1Analytics | Org1 production data scanning with DataSage | mysql | 8       |


## How to add Class
Invoke command as below:
```sh
./datasage-cli class list
```
> Reponse will be as below:

| ID | NAME                                      | DESCRIPTION                                        |
|----|-------------------------------------------|----------------------------------------------------|
| 1  | Phone Number                              | Contains Phone Number                              |
| 2  | Drivers License ID                        | Contains Drivers License ID Number                 |
| 3  | Social Security                           | Contains Social Security Number                    |
| 4  | Passport                                  | Contains Passport Number                           |
| 5  | Taxpayer                                  | Contains Taxpayer Number                           |
| 6  | Electoral Roll                            | Contains Electoral Roll Number                     |
| 7  | National Insurance                        | Contains National Insurance Number                 |
| 8  | Medical Beneficiary                       | Contains Medical Beneficiary Number                |
| 9  | Healthcare Common Procedure Coding System | Contains Healthcare Common Procedure Coding System |
| 10 | Unique Device Identifier                  | Contains Unique Device Identifier                  |
| 11 | Health Insurance Claim                    | Contains Health Insurance Claim Number             |

## How to add Tags
Invoke command as below 
```sh
./datasage-cli tag list
```
> Reponse will be as below:

| ID | NAME  | DESCRIPTION                                         | CLASS                                       |
|----|-------|-----------------------------------------------------|---------------------------------------------|
| 1  | PII   |         Personally Identifiable Information         |                [Phone Number]               |
| 2  | GDPR  |          General Data Protection Regulation         |                [Phone Number]               |
| 3  | GDPR  |          General Data Protection Regulation         |         [Drivers License ID Number]         |
| 4  | PII   |         Personally Identifiable Information         |         [Drivers License ID Number]         |
| 5  | PII   |         Personally Identifiable Information         |           [Social Security Number]          |
| 6  | PII   |         Personally Identifiable Information         |              [Passport Number]              |
| 7  | PII   |         Personally Identifiable Information         |              [Taxpayer Number]              |
| 8  | GDPR  |          General Data Protection Regulation         |              [Taxpayer Number]              |
| 9  | GDPR  |          General Data Protection Regulation         |         [National Insurance Number]         |
| 10 | GDPR  |          General Data Protection Regulation         |           [Electoral Roll Number]           |
| 11 | PHI   |             Protected Health Information            |         [Medical Beneficiary Number]        |
| 12 | PII   |         Personally Identifiable Information         |         [Medical Beneficiary Number]        |
| 13 | PHI   |             Protected Health Information            | [Healthcare Common Procedure Coding System] |
| 14 | PII   |         Personally Identifiable Information         | [Healthcare Common Procedure Coding System] |
| 15 | UDI   |               Unique Device Identifier              |          [Unique Device Identifier]         |
| 16 | HIPAA | Health Insurance Portability and Accountability Act |       [Health Insurance Claim Number]       |

## How to apply Policy

## How to view Logs
To view the scan logs of Org1Analytics complete datasource
Invoke command as below: 
```sh
./datasage-cli datasource  logs -datasource Org1Analytics
```
To view the scan logs of northwind DB of Org1Analytics datasource
```sh
./datasage-cli datasource  logs -datasource Org1Analytics  -database northwind
```
To view the scan logs of employeetable of  northwind DB of Org1Analytics datasource
```sh
./datasage-cli datasource  logs -datasource Org1Analytics  -database northwind -table employee
```

{: .d-inline-block }

 
{: .no_toc }
