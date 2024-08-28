# Overview

Let's create a container. 

In this section, you will see how to containerise the hello-world-rag code. 
We will also see how to access RAG application from curl.

## How to 

- Install and verify that docker is working. 
- 
- Go to the directory hello-world-run is stored.
- Create an image called "hello-world-rag" 
    - `docker build -t hello-world-rag .`
      - DO NOT FORGET the "." 
      - This is to pick Dockerfile by default.
  - To run the docker image, use
    - `docker run -p 5000:80 hello-world-rag`
- From another  terminal, you can run `curl -X POST -H "Content-Type: application/json" -d '{"query": "What does RAG stand for?"}' http://localhost:5000/ask`


### Well done! You created and ran the program from a docker container.