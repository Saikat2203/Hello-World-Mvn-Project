pipeline {
    agent any
    tools {
        maven 'mvn'
    }
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
        stage('Check for Maven') {
            steps {
                sh '''
                echo $JAVA_HOME
                echo $MAVEN_HOME
                echo $M2_HOME '''
            }
        }
        stage('Check Files') {
            steps {
                sh ''' echo 'In Check Files stage'
                ls'''
            }
        }
        stage('Change directory') {
            steps {
                sh ''' cd java-hello-world-webapp/
                echo "Files in java-hello-world-webapp"
                ls '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                    mvn package
                '''
            }
        }
    }
}
