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
                anyof { branch 'production'; branch 'sprint*/release'} 
            }

            steps {
                echo 'Hello production'
            }
        }
    }
}
