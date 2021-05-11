pipeline {
    agent any
    stages {
        stage ('Clone repo and clean it') {
            steps {
                sh "rm -rf my-app"
                sh "git clone https://github.com/Voks1995/my-app.git"
                sh "mvn clean -f my-app"
            }
        }
        stage ('Test') {
            steps {
                sh "mvn test -f my-app"
            }
        }
        stage ('Deploy') {
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}
