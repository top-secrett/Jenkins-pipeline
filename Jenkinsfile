pipeline {
    agent any
    
    stages {
        stage('Chekout'){
            steps {
                git branch: 'main', url: "git@github.com:top-secrett/Jenkins-pipeline.git"
            }
        }
        stage('Deploy') {
            steps {
                sh 'ansible-playbook playbook.yaml'
            }
        }
    }
    
}
