pipeline {
    agent any
    
    environment {
        PRJECT_NAME = 'KARAS'
        OWNER_NAME = 'DIMON'
    }
    
    stages {
        stage('1-Build'){
            steps {
                echo "Start"
                echo "Build....."
                echo "End"
            }
        }
        stage('2-TEsts') {
            steps {
                echo "Test...."
                echo 'Hello ${OWNER_NAME}'
                echo 'Project name in ${PROJECT_NAME}'
                sh '''
                #!/bin/bash
                pwd
                ls -la
                '''
                echo "end test"
            }
        }
        stage('3-Deploy') {
            steps {
                echo 'Start deploy'
            }
        }
        stage('4-congrad') {
            steps {
                echo 'Congrad'
            }
        }
    }
}
