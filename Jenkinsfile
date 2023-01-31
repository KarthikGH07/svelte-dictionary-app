pipeline {
    agent any 
        stages {
            stage ('Test') {
                steps {
                   echo "Testing..." 
                   sh 'npm install'
                   sh 'npm run lint'
                }
            }
        }
}