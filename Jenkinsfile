pipeline {
    agent { docker { image 'openjdk:11-jdk' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                  echo 'Testing..'
                  sh './gradlew test --continue'
            }
            post {
               always {
                    echo 'Test reports'
//                     junit 'build/reports/tests/test/*.html'
               }
            }
        }
        stage('Checkstyle') {
            steps {
                echo 'Checking checkstyle....'
//                 sh './gradlew checkstyleMain checkstyleTest'
            }
        }
    }
}
