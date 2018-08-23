# GCP emulators
## minikube & skaffold
### Requirements
* minikube
* skaffold
### Usage
First of all, you need to launch minikube!!
```
make deploy
```

### docker-compose
```
docker network create gcp-network
docker-compose up

export PUBSUB_EMULATOR_HOST=localhost:8538
export PUBSUB_PROJECT_ID=my-project-id
export DATASTORE_EMULATOR_HOST=localhost:8432
export DATASTORE_PROJECT_ID=my-project-id
curl -XPUT http://localhost:8538/v1/projects/project/topics/the-topic
```

# LICENSE
MIT
