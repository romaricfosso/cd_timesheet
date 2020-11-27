pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                git 'https://github.com/romaricfosso/cd_timesheet.git'
            }
        }
         stage('run') {
            steps {
            sh"javac Main.java"
            }
        }
         stage('Hello') {
            steps {
               sh"java Main"
            }
        }
    }
}
