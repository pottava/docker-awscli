# Dockerized AWS-CLI

[![pottava/awscli](http://dockeri.co/image/pottava/awscli)](https://hub.docker.com/r/pottava/awscli/)

Supported tags and respective `Dockerfile` links:

・latest ([versions/1.14/Dockerfile](https://github.com/pottava/docker-awscli/blob/master/versions/1.14/Dockerfile))  
・1.14 ([versions/1.14/Dockerfile](https://github.com/pottava/docker-awscli/blob/master/versions/1.14/Dockerfile))  
・1.13 ([versions/1.13/Dockerfile](https://github.com/pottava/docker-awscli/blob/master/versions/1.13/Dockerfile))  
・1.12 ([versions/1.12/Dockerfile](https://github.com/pottava/docker-awscli/blob/master/versions/1.12/Dockerfile))  
・1.11 ([versions/1.11/Dockerfile](https://github.com/pottava/docker-awscli/blob/master/versions/1.11/Dockerfile))  
・1.10 ([versions/1.10/Dockerfile](https://github.com/pottava/docker-awscli/blob/master/versions/1.10/Dockerfile))  

### Usage

```
$ docker run --rm pottava/awscli --version
$ docker run --rm -it -v $HOME/.aws:/root/.aws pottava/awscli configure
$ alias aws="docker run --rm -v $HOME/.aws:/root/.aws pottava/awscli"
$ aws ec2 describe-instances
```
