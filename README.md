This image is usable for one image that you can run docker, helm and kubectl in one place (instead of using different images)

using docker example : docker run --rm --name docker-helm-kubectl -v /var/run/docker.sock:/var/run/docker.sock docker-helm-kubectl-alpine:latest docker ps -a

using kubectl or helm example : docker run --rm --name docker-helm-kubectl -v ~/.kube:/root/.kube docker-helm-kubectl-alpine:latest kubectl get pods docker run --rm --name docker-helm-kubectl -v ~/.kube:/root/.kube docker-helm-kubectl-alpine:latest helm list

NOTE: it has to mount inside the contianer as /root/.kube as shown above .

Rebuilding the image without docker : Please check the Dockerfile : just replace the FROM line to be alpine:latest
  
