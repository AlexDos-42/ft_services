# Ft_services

This project consist to clusturing an docker-compose application and deploy it with Kubernetes. 

![screen](https://)

## Instructions

This is the list of commands:
	sh setup.sh instal		Instal minikube
	sh setup.sh start		Start minikube
	sh setup.sh services		Build services
	sh setup.sh clear		Stop and delete services

When the project is running, you can use:
	minikube dashboard
	minikube stop
	minikube delete
	kubectl get service
	kubectl get deployment
	kubectl get pods
If ft_services is running, click on link bellow:
	http://192.168.49.20
To test the ftps server:
	ftp 192.168.49.20 21		to acces ther server
		-> alesanto - password
	put name-of-the-file
	if error 500: use command pass