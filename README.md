# multi-docker
[![Build Status](https://travis-ci.org/theuncleshege/multi-docker.svg?branch=master)](https://travis-ci.org/theuncleshege/multi-docker)

A multiple docker-containerized project hosted on AWS Elastic Beanstalk.

It is a simple Fibonacci calculator but intentionally developed in a complex way to demonstrate how to structure and deploy a CI/CD pipeline with multiple docker containers on AWS.

### [Demo](http://multi-docker-env.eirjju89pu.us-east-2.elasticbeanstalk.com/)

The project is broken down into four (4) different containers:

- Client: The frontend that clients see when they visit the website.
- API: Stores data into and pulls data from Redis and the PostgresSQL database.
- Worker: Responsible for the actual fibonacci computation and stores the result in Redis.
- Nginx: Routes traffic between the Client and API containers based on the URL being accessed.

The tech stack involved in this project include:
- React - For client side development
- Node.js/Express - For REST API development
- Amazon ElastiCache - For Redis
- Amazon RDS - For PostgresSQL database
- Travis CI - For CI/CD
- AWS Elastic Beanstalk - For hosting
