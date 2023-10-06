pipeline {
  agent any
  

    stage('Playbook Nginx') {
      steps {
        sh 'ansiblePlaybook credentialsId: 'privatekey', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml''
      }
    }
  }