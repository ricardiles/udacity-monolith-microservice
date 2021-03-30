# Ricardo Ardiles Udagram Image Filtering Application

## Getting Started

This repository contains excercises and project of Cloud Developer Nanodegree Program. The base code is in [nd9990-c3-microservices-exercises](https://github.com/udacity/nd9990-c3-microservices-exercises/tree/master/project)

## Current project

As we learned in class, this project refactor udagram monolith application into microservices.

I thought is was a great idea separate every microservice in his respectively repository to get isolated deploys. This is the best way to test every docker image creation in Travis CI.  

Anyway I put every microservice in a folder in this repository for your evaluation.  

* [ms-reverse-proxy](https://github.com/ricardiles/ms-udacity-reverse-proxy) 
* [ms-udagram-api-feeds](https://github.com/ricardiles/ms-udacity-api-feeds)
* [ms-udagram-api-users](https://github.com/ricardiles/ms-udacity-api-users)
* [ms-udagram-frontend](https://github.com/ricardiles/ms-udacity-frontend)


In the readme of the [screenshots](ht) you can find more information about what has been done and evidence of the deployment in addition to the tests carried out.

## URL
The proxy was exposed so that it can be tested directly in the following url:  
http://a574601d828a64664afe7f4805c3d98b-698787260.us-west-2.elb.amazonaws.com:8080/api/v0/

So you can test the postman collection replacing host -> http://a574601d828a64664afe7f4805c3d98b-698787260.us-west-2.elb.amazonaws.com:8080/api/v0/

* http://a574601d828a64664afe7f4805c3d98b-698787260.us-west-2.elb.amazonaws.com:8080/api/v0/users
* http://a574601d828a64664afe7f4805c3d98b-698787260.us-west-2.elb.amazonaws.com:8080/api/v0/feed


## Screenshots

In screenshots folder you can find the evidence:

* docker hub
* kubectl get hpa
* kubectl get pods
* kubectl logs feed
* kubectl logs users
* kubectl service feeds
* kubectl service frontend
* kubectl service reverse proxy
* kubectl service users
* travis ci deploy
* travis repositories
* travis success 1
* travis success 2
* travis webhook

## Outputs

In addition to the screenshots I put some txt files with output of the commands:

describe_service.txt
```
kubectl describe service
```

get_hpa.txt
```
kubectl get hpa
```

get_pods.txt
```
kubectl get pods
```

logs_feeds.txt
```
kubectl logs udagram-feeds-app-5cf7bc98f7-tr5qj
```
logs_user.txt
```
kubectl logs udagram-user-app-d7b4b946c-7bvf2
```


## Another considerations

* Exists a .travis.yml file in the root only to get a preview of the .travis.yml file in every microservice. 
* set_env.sh was eliminated from the repository for security reasons.