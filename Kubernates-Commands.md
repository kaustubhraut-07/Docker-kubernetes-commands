# Kubernates Commands

### Kubectl is the main thing to run kubernates commands

### List Down All kubernates Running Kubernetes Containers
kubectl get pods

### List Down All kubernates Running Kubernetes Services
kubectl get services 
kubectl get svc

### List Down All kubernates Running Kubernetes Deployments
kubectl get deployments

### List Down All kubernates Running Kubernetes Jobs
kubectl get jobs

### List Down All kubernates Running Kubernetes CronJobs
kubectl get cronjobs

### List Down All kubernates Running Kubernetes ConfigMaps
kubectl get configmaps

### If we wants to deploy any kubernates pod we can use below command

kubectl apply -f pod.yaml

### If we wants to delete any kubernates pod we can use below command

kubectl delete -f pod.yaml

### Sample kubernates deployment yaml file

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment -> here we needs to gave name of deployment
  labels:
    app: nginx -> label is importtant thing
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx 
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx -> here we needs to provide the name of container
        image: nginx:1.14.2 -> here we needs to provide the name of image like docker image that we have build up
        ports:
        - containerPort: 80 -> also needs to specify the port accoing to the exposed port of container


```

### To get the pod ip address information 

kubectl get pods -o wide -> here we can use wide command to get the pod information with all the  details more sprecificly the ip address detils for each pod

### To get all the detils of pod
kubectl get pods -v=7  -> here v means verbose by using this command we can get the pod information with all the  details more sprecificly the ip address

