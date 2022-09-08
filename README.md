# Handle CI/CD pipeline – Support auto scaling, increase monitoring and etc.
This can be used with [Elastic Beanstalk Multi Docker Container](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_docker_ecs.html).

## AWS Resources this setup uses out of the box
- AWS Elastic Beanstalk will handle deployments.
- AWS Elastic Load Balancer with Auto scaling . Meaning you can have multiple EC2 instances running your app.
- AWS ElastiCache configured as the cache (redis) for laravel
- AWS RDS for the database (mysql is default)
- AWS S3 for storing uploaded assets (e.g. images).
- AWS SQS for queues.
- AWS Cloudfront created for you to use. Env variable `CDN` refers to the CDN address, just use it right away for your assets.

#### Optional
- AWS SNS to send SMS via AWS SNS.
- AWS SES to send emails.

#### The directory structure
Directory structure should now be:
- .ebextensions/
- lavarel/
- .gitignore
- .ebignore
- Dockerrun.aws.json
- README.md


