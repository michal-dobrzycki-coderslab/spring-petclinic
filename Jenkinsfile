pipeline {
    agent any
    tools {
        maven 'Maven 3.8.6'
        jdk 'jdk17'
     } 
    stages {
        stage('Build') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                sh '''
                mvn clean install
                ls
                pwd
                ''' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}