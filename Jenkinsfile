pipeline {
    agent {
        label 'java-project'
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
}
