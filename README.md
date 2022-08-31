[![Build](https://img.shields.io/badge/build-passing-green.svg?style=flat&color=B6D827)](https://choosealicense.com/licenses/mit/) [![Grade](https://img.shields.io/badge/grade-100/100-green.svg?style=flat&color=B6D827)](https://choosealicense.com/licenses/mit/)  



# 🏫 ft_services

This project is a introduction to Kubernetes.

The goal was to create a cluster of docker with differents service into them like Wordpress, PHPMyAdmin, Grafana, NGinx ... and allow them to comunicate with each other.

You can find the subject  for this project [here](https://github.com/gdesant/ft_services/blob/main/ft_services.subject.en.pdf).

# 

[![C](https://img.shields.io/badge/Made&#32;In-BASH-white.svg?style=for-the-badge&color=blue)]()

 Using the [minikube](https://minikube.sigs.k8s.io/docs/), [Kubernetes](https://kubernetes.io/fr/) and [Docker](https://www.docker.com/) 


## Services

In this project you can find docker of multiples services : 

  - [Nginx](https://github.com/gdesant/ft_services/tree/main/srcs/nginx)
  - [Wordpress](https://github.com/gdesant/ft_services/tree/main/srcs/wordpress)
  - [PHPMyAdmin](https://github.com/gdesant/ft_services/tree/main/srcs/phpmyadmin)
  - [MySQL](https://github.com/gdesant/ft_services/tree/main/srcs/mysql)
  - [FTPs](https://github.com/gdesant/ft_services/tree/main/srcs/ftps)
  - [Grafana](https://github.com/gdesant/ft_services/tree/main/srcs/grafana)
  - [InfluxDB](https://github.com/gdesant/ft_services/tree/main/srcs/influxdb)

## Run Locally

Clone the project  
~~~bash  
git clone https://github.com/gdesant/ft_services.git
~~~

Launch
~~~bash  
./setup.sh
~~~

Dashboard 
~~~bash  
minikube dashboard
~~~

## IP and Ports

You can change the IP adresse of the services in the [LoadBalancer](https://github.com/gdesant/ft_services/blob/main/srcs/LBConfigMap.yaml). Default: 172.17.0.3

Each Services have it's own .yaml file where you can change the ports of each services : 

  - [Nginx](https://github.com/gdesant/ft_services/tree/main/srcs/nginx/nginx.yaml) - HTTP: 80, HTTPS: 443
  - [Wordpress](https://github.com/gdesant/ft_services/tree/main/srcs/wordpress/wordpress.yaml) - HTTP: 5050
  - [PHPMyAdmin](https://github.com/gdesant/ft_services/tree/main/srcs/phpmyadmin/phpmyadmin.yaml) - HTTP: 5000
  - [MySQL](https://github.com/gdesant/ft_services/tree/main/srcs/mysql/mysql.yaml) - TCP: 3306
  - [FTPs](https://github.com/gdesant/ft_services/tree/main/srcs/ftps/ftps.yaml) - FTPS: 21, passive-FTPS: 4242
  - [Grafana](https://github.com/gdesant/ft_services/tree/main/srcs/grafana/grafana.yaml) - HTTP: 3000
  - [InfluxDB](https://github.com/gdesant/ft_services/tree/main/srcs/influxdb/influx.yaml) - TCP: 8086

### Be Carful !

Since all the services are connected with each other using their ports. Changing the port of a service may cause some trouble.


# Feedback  

If you have any feedback, please reach out to us at gde-sant@student.42.fr
