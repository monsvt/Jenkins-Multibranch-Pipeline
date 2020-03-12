pipeline {
    agent any 
    stages {
         stage('First') {
             environment{
                EXECUTE = 'True'
             }
              steps {
                  
                  sh """echo 'Step One' """
                  
                    }
            }
         stage('Second') { 
             when { environment EXECUTE: 'True' }
              steps {
                  
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  
              }
            }
         stage ('Third') {
             when { expression {return EXECUTE} } 
              steps { sh """echo 'Step Three' """}
                  }
          }
}
