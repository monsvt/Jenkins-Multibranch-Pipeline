
pipeline {
    agent any 
    stages {
         stage('First') {
             environment{
                env.EXECUTE = true
             }
              steps {
                  
                  sh """echo 'Step One' """
                  
                    }
            }
         stage('Second') { 
             when { expression { env.EXECUTE } }
              steps {
                  
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  
              }
            }
         stage ('Third') {
             when { expression { env.EXECUTE == false } } 
              steps { sh """echo 'Step Three' """ }
                  }
          }
}
