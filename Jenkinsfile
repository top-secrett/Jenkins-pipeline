pipeline {
    agent any
    
    stages {
        stage('Chekout'){
            steps {
                git branch: 'main', url: "git@github.com:Nortsx/jenkinsansiblebook.git"
            }
        }
        stage('Deploy') {
            steps {
                sh 'ansible-playbook playbook.yaml'
            }
        }
    }
    
}
