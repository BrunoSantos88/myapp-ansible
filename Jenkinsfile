pipeline {
  agent any
  

  stages {
    stage('Playbook Nginx') {
      steps {
        sh ansiblePlaybook credentialsId: 'master', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml'
      }
    }
  }
}