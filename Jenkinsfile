pipeline {
    agent {
        label 'java-project'
    }
    enviromment {
        NAME = 'dinesh babu Ramayanam'
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
                echo 'This is Build3'
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
