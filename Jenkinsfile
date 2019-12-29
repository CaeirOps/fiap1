pipeline {
    agent any

    stages {
      stage('Build'){
        steps {
          sh 'docker build -t coredevops:latest .'
        }
      }

      stage('Deploy'){
        steps {
          ansiblePlaybook (
            inventory: 'inventory/',
            playbook: 'playbook.yml',
            colorized: true
          )

          }
        }
    }
}
