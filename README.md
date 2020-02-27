# WebAdvert.Web


Micro-services application for ads with AWS for Cloud hosting and scaling

Below is the architecture being used for these microservices:

![architecture-2](https://pbs.twimg.com/media/ERyQdFQWkAAEXDu.png)

In the above architecture, we are going to use the following

- Add edge caching (users in a different region) [Cloud Front] - Caching
- Application Load Balancer is for x-axis scaling - Cloning EC2 instances
- ECS in this case we are using ECS instead of EC2 as we are deploying containers
- Elastic Cache is for data offloading, so if the service goes down the data will be offloaded.
- RDS is the relational database systems - so instead of creating multiple different databases and paying cost for that use RDS and create multiple different databases inside it. 
- Dynamo Db is basic NOSQL db in AWS.

![architecture](https://pbs.twimg.com/media/ERyQGBbWkAALTNh.png)

In the above architecture, we are going to use the following

- API gateway: aggregates all the APIs to one address -- 
- API gateway has its own caching as well called "API Gateway response cache"
- AWS lamda -- can be a service OUR serverless services per se
- Amazon Cloudwatch - monitoring the health of your system


Other cool things:

Everything is going to be containerized using Docker
Using CI/CD for continuous integration and continuous development
