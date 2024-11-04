pipeline {
    agent {
        label 'agent'
    }
    environment {
          NAME = 'dinesh babu Ramayanam'
          }
    parameters {
        choice(name: 'CHOICE', choices: ['prod', 'dev', 'test'], description: 'select the environment')
    }
    
    stages {
        stage('build') {
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
            steps {
                sh """
                   echo "This stage is Deployment stage"
                """
            }
        }
        stage('buildwithpram') {
          steps {
              echo "choice: ${params.CHOICE}"
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
