pipeline {
      agent none
      stages{
         stage('Build artifact'){
             agent {
                docker {
                    image "maven:3.6.3-jdk-8"
                    args '--entrypoint=""'
                }
             }
             steps{
                sh 'mvn clean install'
                sh 'mkdir demo'
              }
         }        

      }

}
