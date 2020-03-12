
pipeline {
    agent any 
    stages {
         stage('First') {
             environment{
                EXECUTE = true
             }
              steps {
                  
                  sh """echo 'Step One' """
                  
                    }
            }
         stage('Second') { 
             when { expression { EXECUTE == true } }
              steps {
                  
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  
              }
            }
         stage ('Third') {
             when { expression { EXECUTE == true } } 
              steps { sh """echo 'Step Three' """ }
                  }
          }
}
