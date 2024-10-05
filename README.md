# Using the Ansible plugin on a Jenkins multi branch pipeline

Prerequisits:
Install docker https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository

- Run docker daemon to start docker in the background
- Clone the folder and run from the folder: "docker compose up --build -d"
- Run: "docker ps" and search for the id of the "jenkins-main"
- Run: "docker logs <id>" and save the intial Jenkins password
- Install suggested plugins
- enter details...
- set up two nodes, make sure worker1 has label "remote".
- set up multi branch pipeline - use git for source and use repository: "https://github.com/doronfe/jenkins_ansible_task.git", use "Jenkinsfile" for build configuration
- install ansible plugin in Jenkins
- start the multibranch pipeline via parameters only, enter worker2 for "host ip", username and password are "jenkins" - it will run on branch "test_on_this_one"  
