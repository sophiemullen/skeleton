pipeline {
    agent { docker { image 'openjdk:11-jdk' } }

    stages {
        stage('Build') {
            steps {
            sh './gradlew build'
                echo 'Building..'
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
            }
        }
    }
}
