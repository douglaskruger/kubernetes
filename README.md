# kubernetes on Mac
git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core fetch --unshallow 

brew update

brew install minikube

# Minikube Commands

minikube status

minikube version

minikube start

minikube service helloworld

minikube addons enable metrics-server

minikube addons enable dashboard

minikube addons list

minikube dashboard

# Kubectl Commands

kubectl create -f helloworld.yaml 

kubectl get all

kubectl expose deployment helloworld --type=NodePort

kubectl get all

kubectl get nodes

kubectl get deployment/helloworld -o yaml

kubectl get service/helloworld -o yaml

kubectl get pods --seletor env=production

kubectl get pods --seletor env=production --show-labels

kubectl delete pods -l dev-lead=karthik  # where karthik is the label

kubctl create -f helloworld-with-probes.yaml

kubectl get deployments

kubectl get replicaset

kubectl get pods

kubectl get rs # replicasets

kubectl describe deployment <name>

kubectl logs <pod name>

kubectl exec -it <pod name> /bin/bash

kubectl create configmap logger --from-literal=log_level=debug

kubectl get configmaps

kubectl get configmap/logger -o yaml

kubectl create secret generic apikey --from-literal=api_key=123456

kubectl get secrets

kubectl get secret apikey -o yaml

kubectl edit chronjobs\chronjobname 

kubectl get namespaces
