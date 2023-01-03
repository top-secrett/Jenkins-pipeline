pipeline {
    agent any
    
    stages {
        stage('Chekout'){
            steps {
                git branch: 'main', url: "git@github.com:top-secrett/Jenkins-pipeline.git", credebtialsId: 'github-ssh-key'
            }
        }
        stage('Deploy') {
            steps {
                sh 'ansible-playbook playbook.yaml'
            }
        }
    }
    
}
