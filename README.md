# Jenkins
Repo will contain jenkins related information
## Installation of Jenkins using docker

```bash
docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins/jenkins jenkins/jenkins:lts
```
#### Explanation:

- Expose port 8080 -----> Default Runs on that port
- Expose port 50000 ----> Master/Slave communication
- Run in detached mode -> Run container in bakground
- Bind Name Volumes ----> Persist data of jenkins

#### Check docker container is running or not:
```bash
docker ps
```
output:
```bash
CONTAINER ID   IMAGE                 COMMAND                  CREATED          STATUS          PORTS                                                                                      NAMES
fb27d4bf802f   jenkins/jenkins:lts   "/usr/bin/tini -- /u…"   45 seconds ago   Up 38 seconds   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp, 0.0.0.0:50000->50000/tcp, :::50000->50000/tcp   wizardly_raman
```
Check logs to find the password to proceed to installtion:
```bash
docker logs fb27d4bf802f
```
In the logs you will find password copy that.
```bash
Jenkins initial setup is required. An admin user has been created and a password generated.
Please use the following password to proceed to installation:

2ec286d7fbe74926b2e8e71f7c5c56ca

This may also be found at: /var/jenkins_home/secrets/initialAdminPassword
```
Open the   [localhost:8080](http://localhost:8080/) in th browser and put that copy password and continue.
- Click on install suggested plugins
- Create First Admin user
- Finally Jenkins is Ready







