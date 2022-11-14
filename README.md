# Ansible setup

1) Steps to be confiugured on the Jenkins instance (https://docs.google.com/document/d/12nMZu34FppsGQuNRtQW9M2uwOFh7hOg2r8u_tRy2ygM/)
    - Create an Amazon Linux 2 VM instance and call it "jenkins-server"
    - Instance type: t2.medium
    - Security Group (Open): 8080, 9100 and 22 to 0.0.0.0/0
    - Key pair: Select or create a new keypair
    - User data (Copy the following user data): https://github.com/awanmbandi/eagles-batch-devops-projects/blob/maven-nexus-sonarqube-jenkins-install/jenkins-install.sh
    - Launch Instance

2) Steps to be confiugured on the deployment servers together
    - Try to launch 3 EC2 Linux Instances together, call them dev-server, stage-server, prod-server    
    - Count: 3 (to create all of them together)
    - Instance type: t2.micro
    - Security Group (Open): 8080, 9100 and 22 to 0.0.0.0/0
    - Key pair: Select or create a new keypair
    - [User data (Copy the following user data):](userdata.sh)
    - Launch Instances
3) Fill the hosts in the Jenkins server Ansible hosts file as mentioned in (https://docs.google.com/document/d/12nMZu34FppsGQuNRtQW9M2uwOFh7hOg2r8u_tRy2ygM/)

4) Run the pipeline for deployment

