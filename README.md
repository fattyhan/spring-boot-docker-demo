# spring-boot-docker-demo
This a demo for building spring boot project on docker
#BEFORE BUILD
you should install maven、git and docker
#then you should clone the demo on your pc
git clone git clone https://github.com/fattyhan/spring-boot-docker-demo.git
#start your docker
i use the dockertoolbox,if your env is linux or unix you should start it into the install dir
#clean and install project. you can add it to the dockerfile
mvn clean
mvn install
#the build the image
docker build -f dockerfile -t springdocker
#start the image
docker run -p 8080:8080 springdocker
#after then check the ip
docker-machine ls
#request ip:8080
