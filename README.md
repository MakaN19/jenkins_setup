# jenkins_setup
A basic Jenkins setup for experimentation on MacOS.

### Overview
This repository provides a simple setup for Jenkins using Docker on MacOS. It allows you to quickly spin up a 
Jenkins instance for testing and experimentation. Additionally, the setup contains a docker container to emulate 
working with a remote host.

### Run Jenkins with Docker
1. Clone the repository:
```
git clone https://github.com/your-username/jenkins_setup.git
```
2. Navigate to the project directory:
```
cd jenkins_setup
```

3. Run Jenkins using Docker Compose:
```
docker-compose up
```

This will start the Jenkins container, and you can access Jenkins at http://localhost:8080.



### Create local DNS for Jenkins
For a more customized URL to access Jenkins, you can add the following line to your /etc/hosts file:
```
127.0.0.1  jenkins
```

After updating the hosts file, you can access Jenkins at http://jenkins:8080.

### Notes
The Jenkins instance is configured to run on port 8080.
This setup is intended for local experimentation and testing purposes.
Feel free to explore and modify the configuration to suit your specific needs.
