# Example: WordPress and MySQL on Kubernetes

This directory contains the Kubernetes manifest files of the WordPress and
MySQL tutorial for Kubernetes.

Follow this tutorial at https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/.

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
steps 
1.kubectl apply -f . ---------------------> this command will create all resouces needed for the wordpress-app  
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

Regarding ingress
2.Run these commands :
 minikube addons enable ingress to setup ingress controller 
in your local machine find this path " C:\Windows\System32\drivers\etc\hosts "
edit the host file (the host file working as local dns ) edit by below

192.168.49.2 wordpress.local
or sometimes it's not working by minikube ip ..so you need to chnage it by your local machine ip like this :
127.0.0.1  wordpress.local
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
3.You need to start tunnel in minikube 
minikube tunnel

from you browser hit this url :wordpress.local

what happens :
The Ingress controller listens for requests to wordpress.local (which you mapped to 127.0.0.1 in /etc/hosts), and forwards them to the wordpress service on port 80.
