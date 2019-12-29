pipeline {
    agent any

    stages {
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
