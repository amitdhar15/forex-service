pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh './gradlew clean build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'ls -la '
                sh 'cd build'
                echo 'Building....'
                sh 'ls -la '
                sh 'cd libs'
                sh 'ls -la '
                sh 'java -jar forex-services.jar'
            }
        }
    }
}
