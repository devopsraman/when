pipeline {
    agent any 
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Hello build'
            }
        }
        stage('Test') {
             when {
                branch 'master' 
            }
            steps {
                echo 'Hello Test'
            }
        }
        stage('Deliver for development') {
            when {
                branch 'master' 
            }
            steps {
                echo 'Hello master branch'
            }
        }
        stage('Deploy for production') {
            when { 
                anyOf { branch 'production'; branch 'sprint*/*'} 
            }

            steps {
                echo 'Hello production1'
            }
        }
    }
}
