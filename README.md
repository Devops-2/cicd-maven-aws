# apache-maven-web
This is a Web Application build with Maven framework

## Getting Started

These instructions will get you a copy of the project up and running on your on-premise or Cloud servers for development and testing purposes. 

### Prerequisites

* Java > = 8 version
* Maven > = 3 version
* Apache Tomcat > = 7 version

### How to run manually

* Clone this project
* Make Sure you are on the root of the project
* Run the below command
# mvn clean package

### Steps to make this run from CI/CD
* Create Jenkins Job ( Pipeline Or Organisation Bases type)
* Give this GitHub URL as SCM (GIT)
* Seletc the approriate branch
* Give the "JenkinsfileMaven" in the script Path (Jenkinsfile)
* Now, as per the JenkinsfileMaven Code --> It wil get the code, build the code (*.war file) and deploy into tomcat apache
* We need apache tomcat web server, so that we can deploy our *.war file into Web-Server ( Follow the below process)

# Running Apache-Tomcat inside docker container
* Pull this docker image --> ssp25/do-apache-tomcat:v1 
* Above docker image is a ready made apache-tomcat app (tomcat/password --> Manager Gui Creds)
* Use this command --> docker run -dit --rm -p 8080:8080 ssp25/do-apache-tomcat:v1  ( to run the container)
* Now to access use this link --> http://<ec2-instance-Pub-Ip-address>:8080


