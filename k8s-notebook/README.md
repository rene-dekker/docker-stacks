# k8s-notebook
This is a copy of the minimal-notebook with some added libraries:
- kubernetes (cli & python)
- elasticsearch
- curl

# Making image:
export IMAGE=rdtigera/k8s-notebook && docker build -f ./Dockerfile . -t $IMAGE:latest
docker push $IMAGE

# To run in your cluster
$ kubectl apply -f jupyter.yaml
The manifest gives cluster admin permissions to the pod, so you probably wanna change it

The password is set to 'pancake'

