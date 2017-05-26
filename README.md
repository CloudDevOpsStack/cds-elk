# techo-elk
Dockerized ELK(elasticsearch, Logstash and Kibana) tool


#### How to build a new image 

- Checkout repo and cd to its dir
- Build the Image :  
`Docker build -t IMAGENAME .`

Ex: `Docker build -t techo-elk .`
   
   
#### Create a new Jenkins Container on a Docker Host

- Container creation
    - create container: 
        `docker create -p YOURLOCALPORT:5601 -p YOURLOCALPORT:9200 -p YOURLOCALPORT:5044 --name CONTAINERNAME IMAGENAME`
        Ex: `docker create -p 5601:5601 -p 9200:9200 -p 5044:5044 -it --name hertz-elk IMAGENAME`
    - start container: `docker start CONTAINERNAME`
    - Open the Browser console : http://HOSTNAME:5601


#### Ports Configured
- Kibana Port           : 5601
- Lagstash Port         : 5044
- elasticsearch Port    : 9200
