This is Yolo-client Ochestration using kubernetes.
Below are the steps followed.
1.	Install Minikube: Start by installing Minikube on your local machine. Minikube is a tool that allows you to run a single-node Kubernetes cluster locally. 
2.	Start Minikube: Once Minikube is installed, open a terminal and start Minikube by running the command minikube start. This will start a local Kubernetes cluster using a virtual machine.
3.	Verify Kubernetes Installation: After Minikube starts, you can verify the installation by running kubectl version command in the terminal. This will display the version of both the Kubernetes client and server.
4.	Interacting with Minikube Cluster: Now you can interact with your Minikube cluster using kubectl commands. For example, you can run kubectl get nodes to see the nodes in the cluster, or kubectl get pods --all-namespaces to get a list of all the pods in the cluster.
5.	Launch the Minikube dashboard: in the terminal run the command; minikube dashboard.
6.	Deploying Applications: To deploy an application to your Minikube cluster, use the kubectl apply command to deploy and create services. Cd into client and run kubectl apply -f client-deployment.yaml –f client-service.yaml and then cd into backend and run kubectl apply -f deployment.yaml -f service.yaml -f configmap.yaml.
7.	Accessing Services: Once a service is created, you can use kubectl get services to get the external IP address or port that can be used to access your application. You can then use a web browser or other tools to access your application using the provided IP address or port.
8.	Cleaning Up: When you're done with your Minikube cluster, you can stop it by running minikube stop. This will stop the local Kubernetes cluster and free up the resources on your machine. If you want to delete the Minikube cluster entirely, you can run minikube delete.


The images used were containerized using docker.
1. rwambui/yolo-client:1.0.0
2. rwambui/yolo-backend:1.0.0

pvc file is created on the backend folder to provision storage volumes.
The pvc is then used to mount the storage volume to Pods.
PersistentVolumeClaim was used to ensure application's data persists even if the Pod is restarted or rescheduled.