# Kubernetes 

## lauchContainer.yml

- This file will help you to launch container

## ReplicaController.yml

- This file will help you to set replication so that your pod will replicate as soon as it goes down

## LoadBalancerService.yml

- This file helps to create load balancer to manage the traffic in the container

## Webapp

- To launch mysql pod use file **launchMysqlDatabase.yml** or use command `kubectl run pod-name --image=mysql:5.7 --env=MYSQL_ROOT_PASSWORD=pass --env=MYSQL_DATABASE=wpdb --env=MySQL_USER=user-name --env=MYSQL_PASSWORD=pass `

- To login to mysql database use command `mysql -u user-name -ppassword`

- To launch wordpress pod use command `kubectl run pod-name --image=wordpress:5.1.1-php7.3-apache`
  
- Now expose the wordpress pod using command `kubectl expose pod pod-name --type=NodePort --port=80`

- Now got to miniKube and check the Ipaddress using command ` ifconfig eth1`

- Now get the port number using command `kubectl get svc`

- now copy the ip:port in bowser you will find wrodress page 

## Secret.yml 

This file is use to secure credentials but to add credentials in this file first we need to endode data usind [base64](https://www.base64decode.org/)

or we can use command ` Kubectl create secret generic mys --from-literal=p1=password`


