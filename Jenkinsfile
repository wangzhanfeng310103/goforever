pipeline {
    agent any 
    
    stages {
       stage("build & SonarQube analysis") {
           steps {
              // script {
                 // def scannerHome = tool 'ss'
                 //  withSonarQubeEnv('sonar_server') {
                 //   sh "${scannerHome}/bin/sonar-scanner"
                 echo 'building'
              // }
             // }
                               
            }
         }
        stage("Quality Gate") {
           steps {
             // timeout(time: 1, unit: 'HOURS') {
              //  waitForQualityGate abortPipeline: true
             // }
             echo "gate"
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

