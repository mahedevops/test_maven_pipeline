pipeline {
    agent any
    tools {
        maven 'Maven3.1.1'
        jdk 'java8'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "Already Installed Maven"
                '''
            }
        }

        stage ('Build') {
            steps {
                    sh 'cd NumberGenerator & mvn install'
            }
             post {
                success {
                    junit 'NumberGenerator/target/surefire-reports/*.xml'
                        }
                 }
               

           
            }
        }
    
}
