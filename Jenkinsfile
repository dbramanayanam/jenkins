pipeline {
    agent {
        label 'agent'
    }
    environment {
          NAME = 'dinesh babu Ramayanam'
          }
    parameters {
        choice(name: 'action', choices: ['build', 'destroy'], description: 'select the action')
    }
    
    stages {
        stage('build') {
            when {
                 expression { params.action == "build" }
                }
            steps {
                echo 'This is build 2'
            }
        }
        stage('Configure') {
            steps {
                echo 'This is build 2'
            }
        }
        stage('deploy') {
             when {
                 expression { params.action == "deploy" }
                }
            steps {
                sh """
                   echo "This stage is Deployment stage"
                """
            }
        }
    }
  post { 
    always {
        echo 'This will execute always when job executed'
    }
    success {
        sh """
          echo "My name is $NAME"
        """
    }
    unsuccessful {
        echo 'This will execute at them time of job failed'
    }
  }
 }
