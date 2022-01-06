# Migrate MySQL to Oracle ADB using Oracle SQL Developer

## Introduction

This workshop provides step-by-step instuctions for MySQL users, to migrate MySQL database to Oracle Autonomous Database, using Oracle SQL Developer. 

### About this Workshop

If you are considering moving your on-premise MySQL database to the cloud and in the process, also wants to migrate the database to Oracle Database (in our case Autonomous Database - ADB), this workshop will walk you throgh the steps using Oracle SQL Developer v 21.2. This is specially designed, keeping in mind MySQL users, who doesn't have much experience with Oracle Database and Oracle SQL Developer. There are certain prerequisites that you need to have in place, before you start working on core migration lab part. Additional lab references are provided to perform those prerequisites (1 & 2) as well. One of the lab in this workshop provides steps to setup remode desktop connectivity to perform this workshop completely from your own desktop/laptop. 

Estimated Workshop Time: 1.5 hours

![Oracle SQL Developer icon](images/sqldv.jpg " ")

Oracle SQL Developer GUI - Migration Configured 
![Oracle SQL Developer UI](images/sqldevUI.jpg " ")


Oracle SQL Developer is a free, integrated development environment (IDE) that simplifies the development and management of Oracle Database in both traditional and Cloud deployments. SQL Developer also provides migration capability from third-party databases. If you have basic understanding of SQL and know-how of Oracle Cloud and Autonomous Database, it will be quite easy to perform this workshop. However, if you’re coming from MySQL background alone, using this workshop steps, you will still be able to complete the migration. 

### References in this Workshop

The main Oracle document for this migration can be found at the following link, which has been referenced in this post in some places. Wherever I have mentioned “From Doc”, the text is copied from following document and referenced as-is. [SQL Developer: Migrating Third-Party Databases](https://docs.oracle.com/en/database/oracle/sql-developer/21.2/rptug/migrating-third-party-databases.html)


### Objectives

In this workshop, you will learn how to:
* Download Latest Version & Install
* Create Connections for the Target (ADB) database
* Load MySQL JDBC Driver and Source Connection
* Create User for Migration Repository
* Create Migration Connection
* Create Migration Repository
* Complete Migration with the Wizard

### Prerequisites 

For this post, it is assumed that you already have following in place or you can follow the prerequisites labs to set those up:

1. Source: A running MySQL database on-premise, with the necessary network access to target ADB instance as well as Oracle SQL Developer instance. And also database credentials to the source schemas/objects, and sample data in it, which needs to be migrated.

2. Target: ATP (Autonomous Transactions Processing) instance setup in the OCI cloud, with all the required credentials for user, schema and object creation (eg ADMIN user), along with network connectivity (VCN) between SQL Developer and MySQL and ATP database wallet file. We will use this database for Migraiton repository as well. You can equally run this migration on ADW (Autonomous Datawarehouse). Here's a How-to blog post: [Creating an Autonomous Transaction Processing (ATP) Database](https://blogs.oracle.com/weblogicserver/post/creating-an-autonomous-transaction-processing-atp-database).  Or you can follow this lab: [Prerequisite 1 - Create ADB as Target (Optional)] (?lab=adw-connection-wallet). This lab is optional, if you already have an ADB instance (just make sure, your ADB - port 1522 is accessable to SQL Developer instance on-premises or OCI cloud, depending on your scenario).

3. An environment, usually your laptop or another instance in OCI (Oracle Cloud Infrastructure), where you will install and run Oracle SQL Developer. We will follow windows based installation. If you want to set up in OCI cloud, follow this doc: [create Windows instance](https://docs.oracle.com/en-us/iaas/Content/GSG/Reference/overviewworkflowforWindows.htm) and [RDP from your laptop/desktop](https://blogs.oracle.com/pcoe/post/enable-windows-instance-access-via-rdp-on-oracle-compute-cloud-service) (for remote desktop sharing). Or you can also follow this  lab: [Prerequisite 2 - Create Windows VM to run Oracle SQL Developer (Optional)] (?lab=create-windows-vm). If you plan to run SQL Developer from your laptop or any desktop, you can skip this lab (just make sure, your laptop/desktop has access to ADB and MySQL databases/ports)

4. All above 3 environments should have network connectivity among each other, including allowing the required ports for the respective databases (defauts: 1521 for ATP and 3306 for MySQL). Ideally, a VCN for ADB and SQL Developer instances in OCI and a VPN connectivity to MySQL on-premises. 

*Let's get Started!*

Click on the next lab in this workshop to get started.

## Learn More

Ready to learn more?
* Visit our documentation for the latest versions of [Autonomous Database](https://docs.oracle.com/en/cloud/paas/atp-cloud/index.html), [SQL Developer](https://docs.oracle.com/en/database/oracle/sql-developer/21.2/index.html) and [MySQL](https://dev.mysql.com/doc/)
* Try one of our [LiveLabs](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/home?session=110185877771466)
* [SQL Developer FAQ](https://support.oracle.com/epmos/faces/DocumentDisplay?_afrLoop=170592697647624&id=2345874.1&_afrWindowMode=0&_adf.ctrl-state=u1oixgz95_4) from Oracle Support site 
* [Forum for Oracle SQL Developer](https://community.oracle.com/tech/developers/categories/sql_developer)
* [Migration Planning and Methodology](https://www.oracle.com/database/technologies/migration/mig-planning.html)
* [SQL Developer Product Page](https://www.oracle.com/database/technologies/appdev/sqldeveloper-landing.html)
* [MySQL Workbench - Database Migration](https://www.mysql.com/products/workbench/migrate/)


## Acknowledgements
* **Author** - Muhammad Shuja, Principal Cloud Solution Engineer, ODP - ANZ
* **Reviewer** - Person, Org
* **Last Updated By/Date** - Muhammad Shuja, December 2021
