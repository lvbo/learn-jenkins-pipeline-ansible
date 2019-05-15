pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                ansiblePlaybook(
                    playbook: "${env.WORKSPACE}/playbook.yml",
                    inventory: "${env.WORKSPACE}/hosts",
                    credentialsId: 'vagrant'
                )
            }
        }
    }
}