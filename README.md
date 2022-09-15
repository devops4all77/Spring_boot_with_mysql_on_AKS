# Containerized kubernetes app with front end Springboot and backend MySql
Run &amp; Deploy Spring Boot CRUD Orders application built with backend MYSQL and front end Springboot uses PV on Azure.

1. Clone the repository

`git clone https://github.com/devops4all77/Spring_boot_with_mysql_on_AKS.git`  

 `cd Spring_boot_with_mysql_on_AKS/`  

2. Make build using mvn

`mvn install -Dmaven.test.skip=true`  

3. push to the docker repository

`docker push <docke_hub_id>/springbootwithmysql:v1.0`  

4. Create config map and secrets

`alias k=kuebectl`  
`k create -f mysql-secrets.yaml`  
`k create -f mysql-configMap.yaml`  

2. Create MySql database

` k create -f db-deployment.yaml`  

3. Create front end springboot deployment

`k create -f app-deployment.yaml`  
