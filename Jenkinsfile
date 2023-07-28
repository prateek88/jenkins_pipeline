pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh "exit 1"
            }
        }
        stage('Deploy') {
                when {
                  expression {
                    currentBuild.result == null || currentBuild.result == 'SUCCESS' 
                  }
                }
                steps {
                    echo currentBuild.result
                    echo 'Deploying....'
                }
        }
    }
}
