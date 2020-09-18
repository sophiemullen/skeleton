pipeline {
    agent { docker { image 'openjdk:11-jdk' } }

    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh './gradlew build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
