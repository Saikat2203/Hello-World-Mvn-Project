pipeline {
    agent any
    stages {
        stage('git-checkout') {
            steps {
                sh "echo 'in Git checkout'"
            //git 'https://github.com/itaifrenkel/java-hello-world-webapp.git'
            }
        }
        //         stage('git-clone') {
        //             steps {
        //                 //sh 'git clone "https://github.com/itaifrenkel/java-hello-world-webapp.git"'
        //             //git 'https://github.com/itaifrenkel/java-hello-world-webapp.git'
        //             }
        //         }
        stage('Check Files') {
            steps {
                sh ''' echo 'In Check Files stage'
                ls'''
            }
        }
        stage('Change directory') {
            steps {
                sh ''' cd java-hello-world-webapp/
                ls '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                    cd java-hello-world-webapp/
                    mvn package
                '''
            }
        }
    }
}
