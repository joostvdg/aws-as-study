# Study notes

## Important sections
* Messaging
* Deskopt & App Streaming
* Security & Identity
* Management Tools
* Storage
* Database
* Network & Content Delivery
* Compute
* AWS Global Infrastructure (Regions + **A**vailability **Z**ones)

## Important topics
* VPC
* IAM
* SNS
* SQS
* S3

## VPC - Virtual Private Cloud

## CloudFront - AWS Content Delivery Network
* for Edge locations
* not restricted to AWS resources

## S3 - Simple Storage Service
* Object storage
* Files can be up to 5TB
* "unlimited" file storage
* Files are stored in *Buckets* (Folders)
* S3 is a **global** namespace, so any bucket needs to have a unique name
* typical address looks like this: https://s3-eu-west-1.amazonaws.com/acloudguru
* A successful uploaded: HTTP 200 OK
* Built for 99,99% availability
* SLA for 99.9% availability
* Amazon guarantees 99,9 * 11 durabily (99,99999999999)

### Data Consistency Model
* Read after Write consistency for PUTS (for new objects)
* Eventual Consistency for overwrite PUTS and DELETES (can take some time to propagate)

### Key-Value store
* Key
* Value
* Version ID
* Metadata
* Subresources

### Storage tiers
* S3: 99,99% availability, 99,99999999999% durability
* S3-IA (Infrequently Accessed): Storage cost is low cost, but additional costs for retrieval (but direct retrieval)
* Reduced Redundancy Storage: less durability (99,99%) for example, thumbnails that you can regenerate if missing
* Glacier: very cheap, but takes 3-5 hours to retreive

### Notes
Files are stored lexographically (alphabetic order). 
This includes geographical storing.
So storing many files with very similar names at the sametime might run into write bottleneck.

## IAM - Identity Access Management
It is not restricted to a region, always global.
You start with a root account, the original account bound by email address.

New users have no roles, group or permissions.
Any credential they have, you get once and only once.
So either download them or store them. After that you have to regenerate them.

* Centralised control of your AWS account
* Shared access to your AWS account
* Granular permission
* Identity Federarion (AD, Facebook, LinkedIn, OpenID, OAUTH)
* Multifactor Authentication (**MFA**)
* And other standard I&A stuff

### Login Types
* Programmatically (via Access Key)
* Console (via the web GUI)

### Terms
* **Users**: End Users (people)
* **Groups**: A collection of users under one set of permissions
* **Roles**: 
* **Policies**: a document containing permissions for a user, group or role

## SNS

## SQS

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

## Developer Tools
* **CodeCommit**: SCM
* **CodeBuild**: for compiling your code
* **CodeDeploy**: for deploying your code to your AWS stuff
* **CodePipeline**: pipeline as code for AWS

## Mobile Services
* **Mobile Hub**: Basic stuff for the Mobile apps separate console for AWS
* **Cognito**: user credentials for mobile (like using OpendID, OOAUTH etc)
* **DeviceFarm**: like selenium grid
* **Mobile Analytics**: App usage data
* **PinPoint**: user data of your apps

## Business Productivity
* **WorkDocs**: online docs
* **WorkMail**: online mail

## Internet of Things
* **IoT**: for managed all the different devices

## Desktop & App Streaming
* **Workspaces**: for having a workspace, like codenvy, in the cloud
* **AppStream 2.0**: streaming deskopt application to users

## Artificial Intelligence
* **Alexa**: voice service in the cloud (Amazon Echo)
* **Lex**: the api to alexa
* **Polly**: Text to Speach
* **Machine Learning**: allows you predict data based upon previous performance
* **Rekognition**: feed an image and it will return data, tags or facial regocnition (% based)

## Messaging
* **SNS** (**S**imple **N**otification **S**ervices): via email, sms, or publush to http endpoints
* **SQS**: application queue system
* **SES**: Email services
