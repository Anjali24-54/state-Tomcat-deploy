pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                // Checkout the repository from GitHub
                git 'https://github.com/Anjali24-54/state-Tomcat-deploy.git'
                
                // Run the Ansible playbook with the specified parameters
                ansiblePlaybook(
                    credentialsId: '3a1f141a-2cee-4725-8635-9dec7b70c316',  // The Jenkins credential ID for SSH key
                    disableHostKeyChecking: true,  // Disable host key checking for SSH
                    installation: 'myansible',  // The name of your Ansible installation configured in Jenkins
                    inventory: '/home/aanza/.ansible/hosts',  // Path to the inventory file
                    playbook: 'StateP2-tomcat-warfile-deployment.yaml',  // Path to your playbook
                    vaultTmpPath: ''  // You can leave this empty or specify a path if needed
                )
            }
        }
    }
}
