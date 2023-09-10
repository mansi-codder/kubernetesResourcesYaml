kubectl create -f appConfig.yaml

kubectl create configmap \
 app-config --from-literal=APP_COLOR=grey \
            --from-literal=APP_MODE=prod

            kubectl create configmap \
 app-config --from-file=appconfig.properties

 kubectl get configmaps

 kubectl describe configmaps