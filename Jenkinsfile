pipeline {
    agent any 
    stages {
         stage('First') {
             
                env.EXECUTE = true
             
              steps {
                  
                  sh """echo 'Step One' """
                  
                    }
            }
         stage('Second') { 
             when { expression { ${EXECUTE} } }
              steps {
                  
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  
              }
            }
         stage ('Third') {
             when { expression { ${EXECUTE} == false } } 
              steps { sh """echo 'Step Three' """ }
                  }
          }
}
