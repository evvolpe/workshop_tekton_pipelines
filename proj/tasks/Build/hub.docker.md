Docker hub
User winterfoxoutlook
PWD testetektonpipeline!

kubectl create secret docker-registry dockerhub \
  --docker-server=$DOCKER_REGISTRY_SERVER \
  --docker-username=$DOCKER_USER \
  --docker-password=$DOCKER_PASSWORD \
  --docker-email=$DOCKER_EMAIL

  export DOCKER_REGISTRY_SERVER=hub.docker.com

  export DOCKER_USER=winterfoxoutlook

  export DOCKER_PASSWORD=testetektonpipeline!

  export DOCKER_EMAIL=winterfoxit@outlook.com

  kubectl create secret docker-registry dockerhub --docker-server=$DOCKER_REGISTRY_SERVER --docker-username=$DOCKER_USER --docker-password=$DOCKER_PASSWORD --docker-email=$DOCKER_EMAIL

  tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_source:v1 -f proj/tasks/Source/task-source.yaml
tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_source:latest -f proj/tasks/Source/task-source.yaml


tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_build:v1 -f proj/tasks/Build/task-build.yaml
tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_build:latest -f proj/tasks/Build/task-build.yaml


tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_qa:v1 -f proj/tasks/QA/task-qa.yaml
tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_qa:latest -f proj/tasks/QA/task-qa.yaml


tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_security:v1 -f proj/tasks/Security/task-security.yaml
tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_security:latest -f proj/tasks/Security/task-security.yaml


tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_tests:v1 -f proj/tasks/Tests/task-tests.yaml
tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_tests:latest -f proj/tasks/Tests/task-tests.yaml


tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_deploy:v1 -f proj/tasks/Deploy/task-deploy.yaml
tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_deploy:latest -f proj/tasks/Deploy/task-deploy.yaml


tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_finally:v1 -f proj/tasks/Finally/task-finally.yaml
tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_tasks_finally:latest -f proj/tasks/Finally/task-finally.yaml

tkn bundle push index.docker.io/winterfoxoutlook/microservice-api_pipeline:v1 -f proj/pipeline/microservice-api-bundle.yaml