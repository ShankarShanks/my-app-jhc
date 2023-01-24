@Library("javahome-libs") _
pipeline {
  agent any

    stages {
      stage('Maven Build') {
        steps {
          sh 'mvn clean package'
      }
    }
    stage('Deploy to Dev Tomcat') {
      steps {
        tomcatDeploy('172.31.9.112','app','tomcat-dev')
        
@Library("mylibs") _
pipeline {
  agent any
  tools {
    maven 'maven2'
  }
  stages{
    stage("Maven Build"){
      steps{
        sh "mvn clean package"
      }
    }
    stage("Deploy To Dev"){
      steps{
        tomcatDeploy("tomcat-dev","ec2-user",["172.31.13.89","172.31.13.89"])
      }
    }
  }
}
