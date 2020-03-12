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
             when { environment name:'EXECUTE', value: 'True'}
              steps {
                  
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  
              }
            }
         stage ('Third') {
             when { environment name:'EXECUTE', value: 'True' } 
              steps { sh """echo 'Step Three' """}
                  }
          }
}
