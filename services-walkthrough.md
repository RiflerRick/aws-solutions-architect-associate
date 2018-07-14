### AWS Services in a nutshell

Here is a list of all aws services and what each one does in a nutshell. Not all the services listed here are relevant to the solutions architect associate exam.
For the services which are infact relevant to the solutions architect associate exam, a small note is given on the side. 

- **Compute service**(relevant)
    - EC2: virtual machines
    - EC2 container services: run and manage docker containers at scale
    - Elastic beanstalk: Elastic beanstalk is actually for people who do not understand aws. Here we can actually upload code and the service can handle the rest. So all a developer has to worry about is the code.
    - Lambda: Lambda is essentially code that we can upload to the cloud and we can control when it executes. We do not have to worry about physical or virtual machines, there is nothing to manage, there is no OS even.
    - Lightsail: Its amazon's VPS service. This is again meant for people who do not want to understand anything regarding aws. 
    - Batch: This is used for batch computing

- **Storage**(relevant)
    - S3: simple storage service. Object based storage.
    - EFS: Elastic file system. Network attached storage. This is essentially a volume that aws gives where we can store data and later mount that to multiple elastic compute machines.
    - Glacier: data archival, place to store the data for very cheap.
    - Snowball: way to bring in large amounts of data to the amazon data centers bascially physically, so rather than bringing in uploading data through the internet which might cost a lot of data, its better to write it into a disk and have to physically transferred. 
    - Storage Gateway: VMs that you can install in ur office and it would replicate information back to S3
   
- **Databases**(relevant)
    - RDS: MySql, Postgresql, Aurora, Oracle, any relational dbs
    - DynamoDB: for non-relational databases
    - Elasticache: caching commonly queried from the database server. 
    - RedShift: Data warehousing or business intelligence. Used commonly for running really complex database queries.

- **Migration**(relevant)
    - AWS Migration hub: Tracking service that allows us to track applications as we are migrating to a database.
    - Applications Discovery Service: It detects what applications you have and what their dependencies are
    - Database Migration Service: migrating database
    - Server Migration service: once again for migration. This time for migrating servers.
    - Snowball: snowball is actually service of both storage and migration.

- **Networking and content delivery**(relevant)
    - VPC: virtual private cloud. we can think of vpc as a virtual data center. we can configure firewalls and route tables and the like
    - CloudFront: amazon's content delivery network. A possible scenario of the usage of CloudFront could be that we have our videos, music and the like being stored in london and a user in australia would like to fetch these files. CloudFront would actually store these files closer to the user in an edge location so that it is loaded faster in the user's location
    - Route53: amazon's dns service
    - API Gateway: Its a way of creating our own apis for other services to talk to
    - Direct Connect: Way of running a dedicated line from our corporate head office or our data center directly into amazon. 

- **Developer Tools**
    - CodeStar: Project managing code.
    - CodeCommit: Store code essentially
    - CodeBuild: Compile the code, run tests against it and so on.
    - CodeDeploy: Automates application deployments.
    - CodePipeline: CD tool
    - X-Ray: Analyze and debug serverless applications
    - Cloud9: IDE in the cloud

- **Management Tools**(relevant)
    - CloudWatch: Monitoring service
    - CloudFormation: Its essentially a way of scripting infrastructure. So to give a scenario, for a infrastructure architect for instance, his/her job would be to go over and buy servers, load balancers, stack them, buy all the networking gear and properly attach them to be able to use them. CloudFormation essentially turns all that into code. 
    - CloudTrail: Used for logging all changes made in the aws environment 
    - Config: Monitors configuration changes across the aws env.
    - OpsWorks: way of automating envs
    - Service Catalog: way of managing catalogs of it services.
    - Systems manager: managing aws resources. basically used for patch maintenance, say if we would like to roll out a security patch across a large number of ec2 instances, we can use this.
    - Trusted advisor: advise across multiple different disciplines. For instance, it will give us an idea of what ports are open and what not. 
    - Managed services: aws man aged services can help us out in case we do not want to worry about stuff like auto scaling and the like.

- **Media Services**
    - Elastic Transcoder: A possible use case would be that whenever a video is uploaded, it would check how the video would look good on a mobile device and the like.
    - MediaConvert: file based video transcoding service. allows us to create video on demand content for broadcast and multi screening at scale.
    - MediaLive: creates high quality video streams for you to deliver to broadcase televisions. 
    - MediaPackage: prepares and protects media
    - MediaStore: optimized for media storage
    - MediaTailer: targetted advertising into video streams

- **Machine Learning**
    - SageMaker: deep learning
    - Comprehend: Sentiment analysis around data
    - DeepLens: artifically aware camera.(physical device)
    - Lex: AI chatbot
    - Machine Learning: basic ML
    - Polly: text to speech
    - Rekognition: CV essentially, image, video
    - Amazon translate: machine translation service
    - amazon transcribe: for transcription: speech to text

- **Analytics**(relevant)
    - Athena: sql queries on s3 bucket. lets say we have a bunch of excel and csv files in our s3 bucket and we would like to know the name of all employees or the like we can actually use athena for doing that basically running an sql query in the s3 bucket.
    - EMR: elastic map reduce. big data map reduce obviously
    - CloudSearch: search services for aws
    - Elasticsearch service: elasticsearch service
    - Kinesis: kinesis is a way of ingesting large amounts of data into aws. Things like social media feeds or tweets.
    - Kinesis video streaming: lets say we have a whole bunch of people doing video streams. Kinesis allows us to ingest all that data and do processing on it.
    - QuickSight: Amazon's business intelligence tool
    - Data Pipeline: moving data between different services. 
    - Glue: used for ETL(extract transform and load). basically for large amounts of data where we may be required to extract the data, transform it in the way we want to and load it.

- **Security and Identity and Compliance**
    - Identity Access Management: identity access 
    - Cognito: Way of doing a device authentication using google or linked or facebook and the like to temporarily access various aws resources. For an example lets say we have a mobile app that would store its current geographic location into a dynamo db. For authenticatio we can actually g ahead and use Cognito
    - GuardDuty: Monitors malicious activity on aws accounts
    - Inspector: inspector is a service that we can install in a ecbox and we can scan for security vulnerabilities. Inspector generates a report.
    - Macie: scan s3 bucket for personally identifiable information(PII). PIIs can be address, phone numbers, pan numbers and the like
    - Certificate manager: we can get ssl certificates for free
    - CloudHSM: Cloud hardware security module is where we can store information like keys for accessing ec2 instances and the like. 
    - Directory Service: way of integrating microsoft active directory services with aws services.
    - WAF: web application firewall. Stops stuff like sequel injections, cross site scripting and the like.
    - Shield: we can get it by default in many services, for instance cloudfront(the aws cdn), load balancers and the like. Shield is essentially a service to stop DDOS attacks.
    - Artifact: its essentially a way of downloading and inspecting amazon's documentation

- **Mobile Services**
    - Mobile hub: a management console. a mobile hub basically sets up the aws services for us, in case of mobile devices.
    - Pinpoint: Targetted push notifications to drive mobile engagements. 
    - AWS Appsync: automatically updates the data in web and mobile applications in real time. 
    - Device Farm: Testing apps on real life devices.
    - Mobile Analytics: analytics for mobiles.

- **AR/VR(Sumerian)**

- **Application Integration**(relevant)
    - Step functions: Essentially managing different lamda functions and the steps to go through it.
    - Amazon MQ: message queues
    - SNS: notification service
    - SQS: its another queue service.
    - SWF: simple workflow service. 

- **Customer Engagement**
    - Connect: it is a contact center as a service. Its like a call center in the cloud.
    - Simple Email service: email service.

- **Business Productivity**
    - Alexa for Business: 
    - Chime: video conferencing
    - Work docs: dropbox for aws. 
    - WorkMail: kind of like gmail

- **Desktop and App streaming**(relevant)
    - Workspaces: We can have our actual os running in the cloud and we can connect from here. 
    - AppStream: streaming the actual application from the cloud

- **IOT**
    - iOT: iOT
    - iOT device management: managing iOT devices
    - amazon freeRTOS: os for microcontrollers.
    - Greengrass: software that has data caching, local computation, machine learning capabilities for connected devices.

- **Game Development**
    - GameLift: games essentially


