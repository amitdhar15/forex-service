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
                sh 'cd libs'
                sh 'java -jar forex-services.jar'
            }
        }
    }
}
