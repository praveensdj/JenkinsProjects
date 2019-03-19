pipeline {
    agent any
    
    tools {
        maven 'apigee-maven'
        jdk 'Java'
    }
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = %PATH%"
                    echo "M2_HOME = %M2_HOME%"
                '''
            }
        }

        stage ('Build') {
            steps {
                    bat 'cd NumberGenerator & mvn install'
            }
             post {
                success {
                    echo "SUCCESS!!"
                        }
                 }
               

           
            }
        }
    
}
