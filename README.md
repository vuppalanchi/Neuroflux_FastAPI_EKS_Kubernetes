# Neuroflux-FastAPI_EKS_Kubernetes
Neuroflux AI Model scale with Kubernetes

FastAPI & Kubernetes using Series with PyCharm & AWS EKS.

## Prerequisites 
AWS Account and PyCharm in local machine

### Software Installation

- The AWS Command Line Interface (CLI) is a unified tool to manage your AWS services.


- The official CLI for Amazon EKS


- Docker helps developers bring their ideas to life by conquering the complexity of app development.


- Kubernetes / K8s, is an 


-Helm  The package manager for Kubernetes.


- Postgres Open Source Relational Database


Redis open source (BSD licensed), in-memory data structure for store, used as a database, cache, and message broker


nice-dcv (Optional) - Deliver high-performance remote desktop and application streaming. If 
you are interested to run your workload directly in AWS.

## System Dependencies

- Make sure your system is up-to-date.
- Run the below command to install python system 
dependencies along-with postgres driver.

```bash

$ sudo apt-get install libpq-dev python-dev libssl-dev

```



## Python Dependencies

- Installing Python Packages

```bash

$ pip install -r requirements.txt

```

![requirements-install](./misc/images/requirements.gif)

- Running Uvicorn Server

```bash

$ uvicorn main:app --reload

```

## Environment

Make sure to update the environment variables in **ecommerce/config.py**, before starting up the project.


![config-file](./misc/images/env_file.png)



## Celery

Make sure before starting up Celery, redis is up and running.

Command to start celery worker :

```bash
$ celery -A main.celery worker -l info
```
or with execution pool
```bash
$ celery -A main.celery worker -l info --pool=prefork
```



## Testing

Before proceeding make sure you have created a test database in Postgres.




## DockerHub

