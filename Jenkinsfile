pipeline {
    agent {
        label 'java-project'
    }
    environment {
          NAME = 'dinesh babu Ramayanam'
          }
    options {
        timeout(time: 1, unit: 'SECONDS')
    }
    stages {
        stage('build') {
            steps {
                echo 'This is build 1'
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
                   sleep 100
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
        echo 'This will execute when the job is failed'
    }
 }
}
