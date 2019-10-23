# Troubleshooting Amazon RDS on VMware<a name="troubleshooting-rds-on-vmware"></a>

To help troubleshoot problems that you have with Amazon RDS on VMware, you can use the following sections\.

**Topics**
+ [Can't Connect to the RDS Connector](#troubleshooting-rds-on-vmware.connection)
+ [Custom AZ Is Not Active](#troubleshooting-rds-on-vmware.custom-az-not-active)
+ [Can't Create a New Custom AZ](#troubleshooting-rds-on-vmware.cannot-create-custom-az)
+ [Edge Router Can't Ping the ESXi Edge Gateway](#troubleshooting-rds-on-vmware.cannot-create-custom-az)
+ [Error in the OVF Template](#troubleshooting-rds-on-vmware.ovf-template-error)

## Can't Connect to the RDS Connector<a name="troubleshooting-rds-on-vmware.connection"></a>

In this case, you can't connect to the RDS connector on your vSphere cluster\.

The cause for this issue is almost always that one or more of the following values in your \.ovf file are incorrect:
+ The host name
+ IP addresses in the Management Network
+ The custom Availability Zone \(custom AZ\) ID
+ The VPN originator IP address
+ The certificate

To solve the issue when onboarding is not complete, deploy the RDS Edge Router image and correct the values in the \.ovf file\. If a certificate is incorrect, check the output in the `/var/output/log/application.log` file\.

To solve the issue when onboarding is finished, complete the following steps:

1. Delete all of the management VMs associated with onboarding\.

1. Delete any roles created by the VMware Virtual DMZ Environment \(VDME\), if any\.

1. Delete the custom AZ in Amazon RDS\.

1. Complete the onboarding steps for a new custom AZ\.

For more information, see [Onboard Your vSphere Cluster](getting-started-with-rds-on-vmware.onboard.md)\.

## Custom AZ Is Not Active<a name="troubleshooting-rds-on-vmware.custom-az-not-active"></a>

In this case, your custom AZ is not moving from `Unregistered` status to `Active` status\.

To solve the issue, make sure that the custom AZ ID is correct\. Also, make sure that you selected the correct custom AZ\.

## Can't Create a New Custom AZ<a name="troubleshooting-rds-on-vmware.cannot-create-custom-az"></a>

In this case, you can't create a new custom AZ, and the following error can be returned\.

```
Custom Availability Zones quota exceeded.
```

To solve the issue, delete your unused DB instances and unused custom AZs\. If you can't create a new custom AZ after deleting unused DB instances and unused custom AZs, contact AWS Support\.

For information about creating a new custom AZ, see [Creating Additional Custom AZs in a Region](creating-a-custom-az.md)\.

## Edge Router Can't Ping the ESXi Edge Gateway<a name="troubleshooting-rds-on-vmware.cannot-create-custom-az"></a>

In this case, the Edge Router can't ping the ESXi Edge Gateway\.

To solve the issue, check the routing configuration from Edge Router console, and look for errors\. If necessary, dump the routing table, and make sure that routes are correct\.

## Error in the OVF Template<a name="troubleshooting-rds-on-vmware.ovf-template-error"></a>

In this case, there is an error in the OVF template\.

If you haven't completed onboarding, modify the OVF template using the software package option to attempt to solve the issue\.

If you have completed onboarding, complete the following steps to attempt to solve the issue:
+ Delete all your management VMs\.
+ Remove any roles created by VDME\.
+ Delete the custom AZ in Amazon RDS\.
+ Create a new custom AZ\.

For more information about the OVF template, see [Onboard Your vSphere Cluster](getting-started-with-rds-on-vmware.onboard.md)\.

For information about creating a new custom AZ, see [Creating Additional Custom AZs in a Region](creating-a-custom-az.md)\.