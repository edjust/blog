# Blog

## About

The blog app is an application built with microservices architecture, designed to be deployed on a Kubernetes cluster and allows users to create posts and comment on them. 

The microservices interact with each other through REST APIs and event-based communication to perform specific tasks within the application.

To manage and deploy these services in a scalable and efficient way, Docker is used to package all the dependencies required by the application, and Kubernetes is used to orchestrate these services. 

In addition, Ingress Nginx is used to manage traffic between the different services, while Skaffold is used to automate the deployment process in a Kubernetes development environment.

The application also includes a React interface that allows to test the app.

Overall, this repository serves as a starting point for developers who want to learn how to build and deploy microservices using Docker and Kubernetes. It provides a practical example of how to implement a microservices architecture and how to use Docker and Kubernetes to manage and orchestrate collections of services.

## Requirements

- Docker
- Kubernetes
- Ingress Nginx
- Skaffold

## Host

When Kubernetes is used, the application can be host at one single domain, in this case the application is running at posts.com domain as shown in the `ingress-srv.yaml` file. In development environment, we are used to accessing all of our different running servers at localhost. So, we have to trick our computer to connecting to our local machine rather than the real posts.com. 

To do that you can edit the hosts file in your local machine to map the domain posts.com to 127.0.0.1. So, any time you try to go to posts.com that exists somewhere out on the Internet, instead is going to connect to your local machine. 

## Running the app

To run the whole application it's used Skaffold. This tool automate many tasks in a Kubernetes development environment, making it really easy to update code in a running pod and to create/delete all objects tied to a project at once. Run the following command on the root of the project folder.

```bash
$ skaffold dev
```

Open a web browser and go to http://posts.com to access the application.
