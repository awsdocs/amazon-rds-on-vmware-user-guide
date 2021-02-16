# Support for RDS features in Amazon RDS on VMware<a name="rds-feature-support"></a>

The primary use case for Amazon RDS on VMware is to support the Amazon RDS service with your choice of database on a VMware infrastructure\.

The following table shows current Amazon RDS on VMware support for Amazon RDS features\.


****  

| Feature | Supported | Notes | More Information | 
| --- | --- | --- | --- | 
| DB instance provisioning | Yes | — | [Creating an Amazon RDS DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_CommonTasks.Create.html) | 
| Modifying the master user password | No | — | [Modifying an Amazon RDS DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.DBInstance.Modifying.html) | 
| Modifying the DB engine version | Yes | For the PostgreSQL DB engine, RDS on VMware supports version 10\.9\-R1 and 10\.10\-R1\. For the Microsoft SQL Server and MySQL DB engines, RDS on VMware currently only supports one DB engine version\. | [Modifying an Amazon RDS DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.DBInstance.Modifying.html) | 
| Renaming a DB instance | Yes | — | [Renaming a DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_RenameInstance.html) | 
| Rebooting a DB instance | Yes | — | [Rebooting a DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_RebootInstance.html) | 
| Stopping a DB instance | No | — | [Stopping an Amazon RDS DB instance temporarily](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_StopInstance.html) | 
| Starting a DB instance | No | — | [Starting an Amazon RDS DB instance that was previously stopped](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_StartInstance.html) | 
| Multi\-AZ deployments | No | — | [High availability \(Multi\-AZ\) for Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html) | 
| DB parameter groups | No | — | [Working with DB parameter groups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithParamGroups.html) | 
| Read replicas | Yes | Currently, this feature is supported for MySQL and PostgreSQL\. | [Working with read replicas](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html) | 
| Encryption at rest and compliance certification | No | — | [Encrypting Amazon RDS resources](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html) | 
| Tagging Amazon RDS resources | Yes | — | [Tagging Amazon RDS resources](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Tagging.html) | 
| Option groups | No | — | [Working with option groups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithOptionGroups.html) | 
| Modifying the maintenance window | Yes | Modifying the maintenance window is supported, but you can't view or apply maintenance updates\. | [Maintaining a DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_UpgradeDBInstance.Maintenance.html) | 
| Modifying the backup window | No | — | [Working with backups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_StartInstance.html) | 
| DB instance scaling | Yes | Modify the on\-premises DB instance class to scale the DB instance\. |  [Modifying an Amazon RDS DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.DBInstance.Modifying.html) [Choosing the on\-premises DB instance class](db-instance-class-on-premises.md)  | 
| Manual and automatic DB snapshots | Yes | All DB snapshots are stored locally\. DB snapshots aren't stored in Amazon S3\. DB snapshot copying and sharing aren't supported\. | [Creating a DB snapshot](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_CreateSnapshot.html) | 
| Restoring from a DB snapshot | Yes | — | [Restoring from a DB snapshot](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_RestoreFromSnapshot.html) | 
| Point\-in\-time recovery | Yes | Currently, this feature is supported for Microsoft SQL Server, MySQL, and PostgreSQL\. | [Restoring a DB instance to a specified time](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PIT.html) | 
| Enhanced Monitoring | No | — | [Enhanced Monitoring](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Monitoring.OS.html) | 
| Amazon CloudWatch monitoring | Yes | — | [Monitoring with Amazon CloudWatch](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/MonitoringOverview.html#monitoring-cloudwatch) | 
| Publishing database engine logs to Amazon CloudWatch Logs | No | — | [Publishing database engine logs to Amazon CloudWatch Logs](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/MonitoringOverview.html#publishing_cloudwatchlogs) | 
| Event notification | No | — | [Using Amazon RDS event notification](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_Events.html) | 
| Amazon RDS Performance Insights | No | — | [Using Amazon RDS Performance Insights](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PerfInsights.html) | 
| Stored procedures for Amazon RDS for MySQL | Yes | — | [MySQL on Amazon RDS SQL reference](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Appendix.MySQL.SQLRef.html) | 
| Automatic minor engine version upgrade | Yes | RDS on VMware doesn't support importing a DB instance from Amazon S3, so enabling auto minor version upgrade during this operation doesn't apply to RDS on VMware DB instances\. | [ Automatically upgrading the minor engine version](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_UpgradeDBInstance.Upgrading.html#USER_UpgradeDBInstance.Upgrading.AutoMinorVersionUpgrades) | 
| Replication with external databases \(MySQL\) | No | — | [Replication with a MySQL or MariaDB instance running external to Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/MySQL.Procedural.Importing.External.Repl.html) | 
| Importing backups from Amazon S3 \(Microsoft SQL Server\) | No | — | [Importing and exporting SQL Server databases](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/SQLServer.Procedural.Importing.html) | 
| Reserved DB instances | Yes |  You can reserve RDS on VMware DB instances for a period of time\. Reserved RDS on VMware DB instances provide a discount compared to on\-demand DB instance pricing\. Currently, reserved RDS on VMware DB instances are only available with the All Upfront offering type for a one\-year term\. Find terms and definitions for RDS on VMware reserved DB instances at [RDS on VMware pricing](https://aws.amazon.com/rds/vmware/pricing/)\.  | [Reserved DB instances for Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithReservedDBInstances.html) \(for general information about reserved DB instances\) | 

**Note**  
Amazon RDS DB instance classes and storage types don't apply to Amazon RDS on VMware\.