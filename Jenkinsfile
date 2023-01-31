pipeline {
    agent any 
    environment {
        NEW_VERSION = '1.17.0'
        GH_CRED = credentials(gh-credentials)
    }
        stages {
            stage ('Test') {
                when {
                    expression {
                        BRANCH_NAME == 'dev' 
                    }
                }
                steps {
                   echo "Testing..." 
                }
            }
            stage ('Build') {
                steps {
                    echo "Building v${NEW_VERSION}"
                    echo "GH cred ${GH_CRED}"
                }
            }
        }

        post {
            always {
                echo "this always gets printed..."
            }

            success {
                echo "this gets printed when the all stages completes successfully!"
            }

            failure {
                echo "this gets printed when stages fail"
            }
        }
}
