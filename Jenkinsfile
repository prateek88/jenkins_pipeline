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
                sh "exit 0"
            }
        }
        stage('Deploy') {
                when {
                  expression {
                    currentBuild.result == null || currentBuild.result == 'SUCCESS' 
                  }
                }
                steps {
                    echo 'Deploying....'
                }
        }
    }
}
