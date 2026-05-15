pipeline {
    agent any

    triggers {
        pollSCM('H/1 * * * *')
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building application using Maven 1'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests using JUnit'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analysing code using SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan using OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying application to AWS EC2 staging server'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running staging integration tests using Newman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying application to AWS EC2 production server'
            }
        }
    }
}
