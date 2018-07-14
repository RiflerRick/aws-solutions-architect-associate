### AWS Services in a nutshell

- Compute service
    - EC2: virtual machines
    - EC2 container services: run and manage docker containers at scale
    - Elastic beanstalk: Elastic beanstalk is actually for people who do not understand aws. Here we can actually upload code and the service can handle the rest. So all a developer has to worry about is the code.
    - Lambda: Lambda is essentially code that we can upload to the cloud and we can control when it executes. We do not have to worry about physical or virtual machines, there is nothing to manage, there is no OS even.
    - Lightsail: Its amazon's VPS service. This is again meant for people who do not want to understand anything regarding aws. 
    - Batch: This is used for batch computing

- Storage
    - S3: simple storage service. Object based storage.
    - EFS: Elastic file system. Network attached storage. This is essentially a volume that aws gives where we can store data and later mount that to multiple elastic compute machines.
    - Glacier: data archival, place to store the data for very cheap.
    - Snowball: way to bring in large amounts of data to the amazon data centers bascially physically, so rather than bringing in uploading data through the internet which might cost a lot of data, its better to write it into a disk and have to physically transferred. 
    - Storage Gateway: VMs that you can install in ur office and it would replicate information back to S3
   
- Databases
    - RDS: MySql, Postgresql, Aurora, Oracle, any relational dbs
    - DynamoDB: for non-relational databases
    - Elasticache: caching commonly queried from the database server. 
    - RedShift: Data warehousing or business intelligence. Used commonly for running really complex database queries.

- Migration
    - AWS Migration hub: Tracking service that allows us to track applications as we are migrating to a database.
    - Applications Discovery Service: It detects what applications you have and what their dependencies are
    - Database Migration Service: migrating database
    - Server Migration service: once again for migration. This time for migrating servers.
    - 
