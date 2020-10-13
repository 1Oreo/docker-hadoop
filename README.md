This repository is based on big-data-europe's docker-hadoop repository.

# Purpose

The purpose of this project is to allow HIT students to run a hadoop cluster on their local machines.

# Hadoop on Docker

This repository allows users to deploy apache hadoop 3.2.1 on docker using docker-compose.

# Perquisites

## Cloning this repository

The initial thing is to clone this repository. This can be done in several ways:

### Download a zip file

[zip](images/zip.png)

### Git clone

For more advanced users, using the Git CLI tool, and the Git clone command. Paste this command to your CLI in the desired location:

`git clone https://github.com/1Oreo/docker-hadoop.git`

## Installing Docker for Desktop

In order to deploy the cluster, Docker is needed, both for running Docker containers, and to deploy docker containers using Docker Compose.  
Download the installation using the following link:  
[Docker for Desktop](https://www.docker.com/products/docker-desktop)

# Deploy the cluster

Once all the prerequisites are met, we can deploy the cluster on to our Docker. Make sure Docker is up and running (after initializing) before trying to deploy the cluster.

1. Open your CLI (CMD/Powershell on windows, terminal on MacOS/Linux)
2. Change into cloned repository directory
3. [cd.png](images/cd.png)  
4. Run the ofllowing command `docker-compose up`
5. Open a second terminal windows and verify the containers are running using the following command `docker ps`
6. You should see 5 containers running as follows:
7. [dockerps.png](images/dockerps.png)

# Accessing the WEB UIs

Many of the services on Hadoop have a WEB based user interface. When the containers are running appropriately, they can be accessed using a browser pointing to 12.0.0.1 with the appropriate port.

## Accessing History Server

The history server collects the data on Hadoop jobs and shows them in one place. Data such as run time and job name can be viewed using it. Accessing it is being done using port 8088 as follows:  
[http://127.0.0.1:8088](http://127.0.0.1:8088)  
The UI looks as follows:  
[history.png](images/history.png)  
