# minikube-deployment

This is just a simple, local deployment using minikube and kubectl.  

Minikube Install
https://kubernetes.io/docs/tasks/tools/install-minikube/

Kubectl
https://kubernetes.io/docs/tasks/tools/install-kubectl/
	
MiniKube
https://github.com/kubernetes/minikube/releases

Best Practice
https://kubernetes.io/docs/concepts/configuration/overview/

	Exercise 1
	Deploy WordPress and MySQL as detailed:
	https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/
	
	Exercise 2
	Increase the number of WordPress containers in the WordPress deployment to 2
	
	Exercise 3
	Delete both WordPress pods
	Note how they are restored instantly (with different pod names) because of the strategy type in the deployment file

    Exercise 4
	Convert the 2 deployment files (MySQL and WordPress) into individual files as detailed here:
	https://kubernetes.io/docs/concepts/cluster-administration/manage-deployment/
	
	This allows for resources to be organised similar to Terraform

    Exercise 5
	Upgrade the image of WordPress to a new version: 
		Find the latest version
		Convert the deployment to a rolling update
		Update the image via the deployment file
		Apply the updated deployment file
            Monitor the rollout status to view the status of the existing and new containers

## Some Helpful Commands

*minikube start* - Launches a minikube VM in virtualbox 

*minikube dashboard* - launches a browser which shows all the pods, containers, deployments that are running

*minikube stop* - Shuts down the VM

*kubectl get deployments --namespace=wordpress* - Shows all your wordpress deployments

*kubectl get pods* - Shows all pods running

*kubectl scale --replicas 2 deployments wordpress* - Using kubectl to scale your deployment and create 2 replicas

