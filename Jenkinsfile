@Library('app-libs') _
pipeline{
    agent any
    stages{
        
        stage("Maven Build"){
            steps{
                sh 'mvn clean package'
                sh 'mv target/myweb*.war target/myweb.war'
            }
        }
        
        stage("Deploy to Tomcat Development"){
            steps{
               tomcatDeploy("172.31.46.32","tomcat-dev","myweb")
            }
        }
    }
    post {
      always {
        cleanWs()
      }
    }
=======
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
