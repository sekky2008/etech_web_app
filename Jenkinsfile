pipeline {
agent any 
  tools {
  maven 'maven'
  }
  stages{
    stage('git-clone'){
    checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/etechDevops/etech_web_app']]])
    }
  }
}
