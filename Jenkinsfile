 @Library('jenkins-shared-library') _
 pipeline {
      agent any //{
       // label "ws"
    //}
    stages{
        stage('Lint Checks'){
          steps {
              script {
                sample.info("user")
            }
            sh "whoami"
            sh "echo ***** Starting Style Checks *****"
            sh "ls -ltr server.js"
            sh "/home/centos/node_modules/jslint/bin/jslint.js server.js || true" // this cmd does style check for server.js
             sh "echo ***** Completed Style Checks *****"
        }
          
    }
        stage('Static Code Analysis'){
          steps {
            sh "echo ***** Starting Static Code Analysis *****"
          //  sh "/home/centos/node_modules/jslint/bin/jslint.js server.js" // this cmd does style check for server.js
           //  sh "echo ***** Completed Style Checks *****"
        }
          
    }

  }
}