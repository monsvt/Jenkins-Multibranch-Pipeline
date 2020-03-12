
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
             when { expression { return EXECUTE } }
              steps {
                  
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  
              }
            }
         stage ('Third') {
             when { expression { return EXECUTE } } 
              steps { sh """echo 'Step Three' """ }
                  }
          }
}
