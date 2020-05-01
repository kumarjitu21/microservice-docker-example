# Sample SpringBoot Application which you can use to create docker image and deploy into Kubernetes Cluster


## To generate Kubernetes Deployment and Service Yaml

  $ kubectl create deployment demo --image=springguides/demo --dry-run -o=yaml > deployment.yaml

  $ kubectl create service clusterip demo --tcp=8080:8080 --dry-run=client -o=yaml >> service.yaml

## Deploy into Kubernetes Cluster

  $ kubectl create -f deployment.yaml

  $ kubectl create -f service.yaml
