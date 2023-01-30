pipeline {
    agent any
    stages {
        stage('git-checkout') {
            steps {
                sh "echo 'in Git checkout'"
                git 'https://github.com/Saikat2203/Hello-World-Mvn-Project.git'
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
