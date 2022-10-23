pipeline {
    agent any


    stages {
        stage('build') {
            steps {
                echo 'Building library'
            }
        }

        stage('test') {          
            steps {
                echo 'Testing library'               
            }
        }

        stage('deploy') {
            steps {
                echo 'Deploying library'
            }
        }
    }

    post {
        success {
            echo 'Successfully built library'
        }

        failure {
            echo 'Library build failed'
        }
    }
}
