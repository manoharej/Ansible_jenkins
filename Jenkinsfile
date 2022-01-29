pipeline {
    agent any
    stages {
        stage('Git clone') {
            steps {
                git branch: 'main', credentialsId: 'git', url: 'https://github.com/manoharej/Ansible_jenkins.git'
            }
        }
       
        stage('Execute ansible playbook') {
            steps {
                ansiblePlaybook credentialsId: 'ansbile', disableHostKeyChecking: true, installation: 'Ansibl2', inventory: 'dev.inv', playbook: 'installhttpd.yaml'
            }
        }
    }
}
