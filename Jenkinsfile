pipeline {
    agent any 
    
    stages {
       stage("build & SonarQube analysis") {
           agent any
           steps {
               def scannerHome = tool 'ss'
               withSonarQubeEnv('sonar_server') {
                   sh "${scannerHome}/bin/sonar-scanner"
               }
                               
            }
         }
        stage("Quality Gate") {
           steps {
              timeout(time: 1, unit: 'HOURS') {
                waitForQualityGate abortPipeline: true
              }
            }
        }
        stage('Test') {            
            steps {                
                echo 'Testing'
                echo 'Test end'            
            }        
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }   
        }    
    }
}

