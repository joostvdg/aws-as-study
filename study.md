# Study notes

## Important sections
* VPC
* IAM

## VPC

## IAM


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
* **Kinesis**: big data analysis (streams)
* **Data pipeline**: move data from service X to service Y
* **Quick Sight**: business analytics tool

## Security & Identity
* **IAM**: fundamental identity federation service
* **Inspector**: examines VM's
* **Certificate Manager**: for SSL cert's
* **Directory Service**: for Active Directory
* **WAF** (**W**eb **A**pplication **F**irewall): security filters for applications
* **Artifacts**: documentation? (Compliance reports) compliance documents (for ISO xxx)

## Management Tools
* **Cloud Watch**: used to monitor the performance of your AWS stuff
* **Cloud Formation**: infrastructure as code! (*"Fuck Yeah!"* - free by me) (maybe use the deep dive course?!)
* **Cloud Trail**: (log) audit trail
* **Opsworks**: automating deployments using Chef (mostly for sysops)
* **Config (Manager)**: auditing your own env. you setup alerts
* **Trusted Advisor**: paperclip for AWS

## Application Services
* **Step Functions**: visualizing what is going on in your own applications
* **SWF** (**S**imple **W**ork**f**low Services): for work flow's (like logistics)
* **API Gateway**: for API management for backend services / LAMBDA etc.
* **AppStream**: for streaming applications to desktop users
* **Elastic Transcoder**: for transcoding data (or video) streams into all usable formats
