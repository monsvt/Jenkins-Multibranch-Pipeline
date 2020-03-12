pipeline {
    agent any 
    environment{
        EXECUTE = true
    }
    stages {
         stage('First') {
             
             
              steps {
                  
                  sh """echo 'Step One' """
                  
                    }
            }
         stage('Second') { 
             when { expression EXECUTE } }
              steps {
                  
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  
              }
            }
         stage ('Third') {
             when { expression { EXECUTE == false } } 
              steps { sh """echo 'Step Three' """ }
                  }
          }

