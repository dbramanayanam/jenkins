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
post { 
    always {
        echo 'This will execute alway when job executed'
    }
    success {
        echo 'This will execute only when the job is successfuol'
    }
    unsuccessful {
        echo 'This will execute when the job is failed'
    }
}
