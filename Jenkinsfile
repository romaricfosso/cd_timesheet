pipeline {
   agent{
       stages{

   
        stage('clone') {
           
       checkout scm
        }
         stage('Build image') {
            steps {
            
            sh ' docker.build("romaric/nginx")'

            }
        }
         stage('Run image') {
            steps {
              
             docker.image('romaric/nginx').withRun('-p 81:81')
             {
              c->
              sh 'docker ps'
              sh 'curl localhost'
              }
            }
        }
    }
}
}
