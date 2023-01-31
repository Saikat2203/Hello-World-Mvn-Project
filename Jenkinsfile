pipeline {
    agent any
    tools {
        maven 'mvn'
        JDK 'java'
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
                sh ''' cd /var/lib/jenkins/workspace/Mvn_Web_Git_Pipeline/java-hello-world-webapp/
                echo "Files in java-hello-world-webapp"
                ls '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                    cd /var/lib/jenkins/workspace/Mvn_Web_Git_Pipeline/java-hello-world-webapp/
                    pwd
                    mvn clean install
                '''
            }
        }
    }
}
