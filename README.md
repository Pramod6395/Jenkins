# Jenkins
Repo will contain jenkins related information
## Installation of Jenkins using docker

```bash
docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins/jenkins jenkins/jenkins:lts
```
Explanation:

- Expose port 8080 -----> Default Runs on that port
- Expose port 50000 ----> Master/Slave communication
- Run in detached mode -> Run container in bakground
- Bind Name Volumes ----> Persist data of jenkins
