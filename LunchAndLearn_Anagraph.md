### Lunch and Learn with Anagraph

#### Vincent Sarago

<p align="left">
<a>@_VincentS_</a><br>
<a>github.com/vincentsarago</a>
</p>


<img width="61" alt="vincent" src="https://user-images.githubusercontent.com/10407788/49164463-29660680-f2fd-11e8-86df-08225f92c35c.png">


# Amazon Web Services

https://console.aws.amazon.com/console/home?region=us-east-1

<p align="center">
  <img src="https://user-images.githubusercontent.com/10407788/49164220-ae045500-f2fc-11e8-89aa-0d2f4c32e714.png">
</p>

## Regions

https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/

<p align="center">
  <img src="https://user-images.githubusercontent.com/10407788/49167746-08ed7a80-f304-11e8-98f6-18c6d005de98.png">
</p>

## S3 `(Storage)``


## EC2 `(Heavy processing / App)``



## ECS `(Run with Docker/Kubernetes)``

EC2 Cluster + Containers

or

Fargate (you only provide containers)

https://github.com/mapbox/ecs-watchbot
https://github.com/vincentsarago/ecs-watchbot-fargate

## AWS Lambda `(code only)``
- You only provide the code
- Scale up and down fast
- Plug to lot of events (SQS, Alaram ...)
- Cheap
- Limit to 15min runtime
- For small processes only (3Go memory, 512Mb disk)
- Supports Node and Python

<img width="279" alt="capture d ecran le 2018-11-28 a 11 21 02" src="https://user-images.githubusercontent.com/10407788/49165665-b4e09700-f2ff-11e8-8f1e-16c0a28af79b.png">

#### Using Python in Lambda
https://blog.mapbox.com/aws-lambda-python-magic-e0f6a407ffc6
https://github.com/mapbox/aws-lambda-python-packages

<p align="center">
  <img src="https://user-images.githubusercontent.com/10407788/49165490-54e9f080-f2ff-11e8-9731-6c432ebd1ccf.jpg">
</p>

## Batch `(~ ecs-watchbot + Fargate)``

## DynamoDB / RDS `(Database)`

## SQS `(Queue)`

## SNS `(Message)`

## Code Pipeline + CodeBuild `(Integration and deployement)``
