## https://kubernetes.io/docs/concepts/configuration/secret/#protections
## https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/

kubectl create secret docker-registry myregistrykey --docker-server=https://index.docker.io/v1/ \
        --docker-username=DUMMY_USERNAME --docker-password=DUMMY_DOCKER_PASSWORD \
        --docker-email=DUMMY_DOCKER_EMAIL

kubectl create secret docker-registry myregistrykey --docker-server='https://index.docker.io/v1' --docker-username='mansidev' --docker-password='Sahil@1428' --docker-email='mansigandhi456@gmail.com'

[System.Environment]::SetEnvironmentVariable('KUBE_EDITOR','code -w')

 [System.Environment]::GetEnvironmentVariable('KUBE_EDITOR')