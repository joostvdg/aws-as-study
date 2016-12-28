# Study notes

## Important sections
* VPC

## VPC

## Networking & Content Delivery
* **VPC**
* **Route53**: For create dns routes.
* **Cloud Front**: part of the CDN?
* **Direct Connect**: like a fixed line

## Compute
* **EC2**: VM's
* **EC2 Container Service**: containers on the VM's, docker on EC2, **Not in exam** (separate course!)
* **Elastic Bean**: deployment platform, more for the developer exam
* **Lambda**: serverless functions
* **Lightsail**: press of the button clouds? **Not in exam**

## Storage
* **S3** (**S**imple **S**torage **S**ervice): virtual disk, **object** storage
* **Glacier**: cold storage / data archives
* **EFS** (**E**lastic **F**ile **S**torage): **block** storage
* **Storage Gateway**: connection gateway between **S3** and your on premise network (via VM?)

## Databases
* **RDS** (**R**elational **D**atabase **S**ervice): standard RDBMS
* **DynamoDB**: **NoSQL** database
* **Redshift**: datawarehouse solution
* **Elasticache**: caching service

## Migration
* **Snowball**: appliance for migrating your on premise storage to AWS (soon also includes AWS services for computing power)
* **DMS**: for migrating databases to AWS, allows you to migrate from a on premise oracle to a different database in AWS
* **SMS** (**S**erver **M**igration **S**ervice): for migrating virtual machines (like VMWare)

## Analytics
* **Athena**: for json analysis
* **EMR**: elastic map reduce (log analysis, etc)
* **Cloud Search**: fully managed service managed by AWS
* **Elastic Search**: I assume it uses ES underneath
