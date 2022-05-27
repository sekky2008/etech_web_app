pipeline {
agent any 
  tools {
  maven 'maven'
  }
  stages{
    stage('git-clone'){
      steps {
    checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/etechDevops/etech_web_app']]])
    }
    }
    stage('k8s-test'){
      steps{
      sh ' kubectl get pods -n kube-system '
      }
    }
  }
}
