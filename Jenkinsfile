pipeline {
      agent any
      stages{
         stage('Build artifact'){
             steps{
                sh 'mvn clean install'
              }
         }
         stage('Build docker image'){
             steps{
                sh 'echo "build docker image"'
              }
         }
         stage('push docker image'){
             steps{
                sh 'echo "push docker image"'
              }
         }
         stage('Deploy on kubernetes'){
             steps{
                sh 'echo "deploy on k8"'
              }
         }

      }

}
