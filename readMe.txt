Steps : 

1- Install Krew which helps you: discover kubectl plugins, install them on your machine, and keep the installed plugins up-to-date.
https://krew.sigs.k8s.io/docs/user-guide/setup/install/

2- Use krew to install the MINIO operator using : 
`kubectl krew update`
`kubectl krew install minio`

3- Use the Kubernetes plugin to init the minio operator and the console : 
   ---> The command below is gonna create and apply all the needed file to start the operator and the console
`kubectl minio init` 

4- Run the following command to create a local proxy to the MinIO Operator Console:
kubectl minio proxy -n minio-operator

5- Using the console you can create tenants :
Tenant : A tenant is a group of users who share a common access with specific privileges to the software instance.

Use on server because in the minikube we have only 1 pod 

6- Run the command below to get the external A proxy to the service : 

minikube service minio -n NAMESAPCE --url


7- Use the client and the Access key in the project and also the url that u got in the step 6


HAPPY CODING
