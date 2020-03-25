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
                
                
                dir("build/libs") {
                        sh "pwd"
                        sh 'ls -la'
                        sh 'java -jar forex-service.jar'
                                }
                
                
                
                
                
                
            }
        }
    }
}
