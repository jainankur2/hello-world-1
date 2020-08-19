pipeline {
      agent any
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
         stage('Build docker image'){
             steps{
                sh 'echo "build docker image"'
                sh 'ls -ll'
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
