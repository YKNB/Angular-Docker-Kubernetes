# create an angular app

ng new nom_app

# Build Angular app

ng build --prod

# Create DockerFile
create file Dockerfile
# Build docker image

docker build -t ng-docker-k8s:1.0 .

# Create Deployment & Service object using yaml

create file ng-deployment.yaml
# mac : passer la variable env-docker a minikube for kubernete
$ eval $(minikube docker-env)

# Deploy app to kubernetes
passer les configurations du fichier .yam a kubernete : kubectl apply -f ng-deployment.yaml 
verfier que le deploiement run : kubectl get deployments
verifier les instances ou replicas creer par le fichier .yam : kubectl get pods
verfier que le service kubenete pour l'application run : kubectl get svc
verifier l'execution de node par kubernete : kubectl get nodes -o wide
