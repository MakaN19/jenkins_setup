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


### SSH keys
The simple setup allows to SSH into the remote host and run simple commands.  
```bash
ssh remot_user@remote_host 'bash -c "your_command with arguments"'
```
To do that, you should configure the SSH setup:
1. Generate SSH key pair on your local machine:
```
ssh-keygen -f "remote-key"
```
This process will create two files: a remote_key (a private key) and a remote_key.pub (a public key)
2. Copy the public key to the remote host (already done in Dockerfile).

3. Add the private key to the Jenkins credentials (already done in Jenkinsfile).

### Notes
The Jenkins instance is configured to run on port 8080.
This setup is intended for local experimentation and testing purposes.
Feel free to explore and modify the configuration to suit your specific needs.
