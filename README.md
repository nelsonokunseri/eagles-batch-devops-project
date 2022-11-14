# Jenkins CI/CD Pipeline for Terraform Infra Project Deployment Project Architecture


# Jenkins Infra CI/CD Pipeline Environment Setup 

1) Jenkins/Terraform
    - Create an Amazon Linux 2 VM instance and call it "jenkins-server"
    - Instance type: t2.medium
    - Security Group (Open): 8080, 9100 and 22 to 0.0.0.0/0
    - Key pair: Select or create a new keypair
    - User data (Copy the following user data): https://github.com/awanmbandi/eagles-batch-devops-projects/blob/maven-nexus-sonarqube-jenkins-install/jenkins-install.sh
    - Launch Instance

2) Copy your Jenkins Public IP Address and paste on the browser = ExternalIP:8080
    - Login to your Jenkins instance using your Shell (GitBash or your Mac Terminal)
    - Copy the Path from the Jenkins UI to get the Administrator Password
        - Run: `sudo cat /var/lib/jenkins/secrets/initialAdminPassword`
        - Copy the password and login to Jenkins
    - Plugins: Choose Install Suggested Plugings 
    - Provide 
        - Username: admin
        - Password: admin
        - Name and Email can also be admin. You can use `admin` all through as we
    - Continue and Start using Jenkins

2) Once on the Jenkins Dashboard
    - Click on "Manage Jenkins"
    - Click on "Plugin Manager"
    - Click "Available"
    - Search and Install the following Plugings "Install Without Restart"
        - Terraform Plugin          
    - Install all plugings without restart 

3) Confirm and make test your installations/setups  

4) Once on the Jenkins Dashboard
    - Click on "Manage Jenkins"
    - Click on "Global Tool Configuration" & Go to section Terraform
    - Click on "Add Terraform"
    - Fill the name as "Terraform" --> Enable "Install automatically" --> Select the latest Terraform version to install     
    - Click on apply and save

