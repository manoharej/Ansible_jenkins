pipeline{
    stages{
        stage {
            steps('GIT SCM'){
                git 'https://github.com/manoharej/Ansible_jenkins.git'
            } 
        }
        
        stage {
            steps('Execute Ansile playbook'){
                ansiblePlaybook become: true, credentialsId: 'ansbile', disableHostKeyChecking: true, installation: 'Ansibl2', inventory: 'dev.inv', playbook: 'installhttpd.yaml'
            } 
        }
    }
    
}
