# Multi AZ

## How do you achieve this High availability?

In Multi-AZ deployment, Amazon RDS provides high availability and durability for DB instances, making them a natural fit for production database workloads. When you provision a Multi-AZ DB instance, Amazon RDS creates a primary DB instance, and synchronously replicates the data to standby instance in a different AZ (Availability Zone). Each AZ runs its own physically distinct, independent infrastructure and it is highly reliable.

## What are the availability zones?

Amazon EC2 is hosted in multiple locations world-wide. These locations are composed of Regions, Availability Zones, and Local Zones. Each Region is a separate geographic area. Each Region has multiple, isolated locations known as Availability Zones.


## How do you set up a multi availability zone infrastructure

Using the AWS Management Console, you can easily create new Multi-AZ deployments or modify existing Single-AZ instances to become Multi-AZ deployments.

To create a new Multi-AZ deployment using the AWS Management Console, simply click the "Yes" option for "Multi-AZ Deployment" when launching a DB Instance.

To convert an existing Single-AZ DB Instance to a Multi-AZ deployment, use the "Modify" option corresponding to your DB Instance in the AWS Management Console.

**Author**

**Zack Davenport** - *Junior DevOps Engineer* - Davenport70
