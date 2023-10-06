pipeline {
  agent any
  

  stages {
    stage('Hello') {
      steps {
        sh '''
          ansible --version
          ansible-playbook --version
          ansible-galaxy --version
        '''
      }
    }

    stage('Playbook Nginx') {
      steps {
        sh 'ansiblePlaybook credentialsId: 'privatekey', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml''
      }
    }
  }
}