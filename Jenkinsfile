pipeline {
    agent any
    stages {
        stage('git-checkout') {
            steps {
                sh "echo 'in Git checkout'"
                //git 'https://github.com/itaifrenkel/java-hello-world-webapp.git'
            }
        }
        stage('Check Files') {
            steps {
                sh ''' echo 'In Check Files stage'
                ls'''
            }
        }
    }
}
