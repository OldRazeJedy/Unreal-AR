pipeline {
    agent {
    node {
      label 'my-defined-label'
      customWorkspace 'F:\\JenkinsJobs\\UnrealAR'
		}
	}


    stages {
        stage('build') {
            steps {
                echo 'Building library'
				bat "G:\\UE4\\UE_4.27\\Engine\\Build\\BatchFiles\\RunUAT.bat BuildCookRun -project=F:\\Practice\\EducationAR\\EducationAR.uproject -platform=Android -clientconfig=Development -cook -stage --pak -package -allmaps"
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
