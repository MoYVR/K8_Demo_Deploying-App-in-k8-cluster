# MongoDB and Mongo Express on Kubernetes

This is an example configuration for deploying MongoDB and Mongo Express on Kubernetes using a deployment and a service. This configuration creates a Kubernetes deployment and a Kubernetes service for both MongoDB and Mongo Express. It also uses a Kubernetes ConfigMap and a Kubernetes Secret to store sensitive information.

## Prerequisites
Before deploying, ensure that Kubernetes is installed and running. 

## Configuration files
This repository contains four configuration files:

1. mongo-configmap.yaml - A Kubernetes ConfigMap file that contains a database URL
2. mongo-express.yaml - A Kubernetes deployment and service for Mongo Express
3. mongo-secret.yaml - A Kubernetes Secret that contains a MongoDB username and password
4. mongo.yaml - A Kubernetes deployment and service for MongoDB

## Deploying
1. Clone this repository.
2. Open a terminal in the root directory of the cloned repository.
3. Deploy MongoDB and Mongo Express using the following command: `kubectl apply -f .`
4. Verify that the pods are running by running the command: `kubectl get pods`

## Usage
After the pods are running, access Mongo Express by opening a browser and navigating to the public IP address of the Kubernetes cluster on port 30000. You should be able to log in with the MongoDB username and password specified in the mongo-secret.yaml file.
