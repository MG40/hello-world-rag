# Overview

Let's run the container from a kubernetes cluster.

In this section, we will run the hello-world-rag container in a kubernetes environment. 
We will also see how to access RAG application from curl.

## How to 

- Install and verify that minikube is working. 
- 
- Go to the directory deployment file is stored.
- Create the deployment and service using 
    - `kubectl apply -f hell-world-rag-deployment.yaml`
    - Run `kubectl get deploy`
      - wait for all pods to get ready
      - You should see something like this
          NAME                         READY   UP-TO-DATE   AVAILABLE   AGE
          hello-world-rag-deployment   1/1     1            1           6m56s
    - Run `minikube service hello-world-rag-service --url`
      - Check for the output
- From another  terminal, you can run `curl -X POST -H "Content-Type: application/json" -d '{"query": "What does RAG stand for?"}' http://<minikube-ip>:<service-port>/ask`
** REPLACE with Minikube IP and port in the above curl**

### Well done! You ran the RAG model in a k8s environment.