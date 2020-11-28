pipeline {
    def app

   
        stage('clone') {
            #steps {
             #   git 'https://github.com/romaricfosso/cd_timesheet.git'
            #}
       checkout scm
        }
         stage('Build image') {
            steps {
            #sh"javac Main.java"
            app= docker.build("romaric/nginx")

            }
        }
         stage('Run image') {
            steps {
              # sh"java Main"
             docker.image('romaric/nginx').withRun('-p 81:81')
             {
              c->
              sh 'docker ps'
              sh 'curl localhost'
              }
            }
        }
    
}
