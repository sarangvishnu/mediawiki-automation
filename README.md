# mediawiki-automation
Files needed for a demo of deploying mediawiki to kubernetes

## Prerequisites
* docker
* a kubernetes cluster
* a copy of mediawiki/core moved into this repo


## Instructions
* $ docker build -t (your tag name) .
* docker push to your docker registry if needed
* update any config values in deployment.yaml
* $ kubectl apply -f deployment.yaml
  * $ kubectl get pods
  * $ kubectl exec (mediawiki pod name) -- /var/config/setup.sh
* $ kubectl apply -f service.yaml
