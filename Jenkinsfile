pipeline {
    agent any 
    stages {
         stage('First') {
              steps {
                  script {
                  EXECUTE = True
                  sh """echo 'Step One' """
                  }
                    }
            }
         stage('Second') { 
             when { $EXECUTE == True }
              steps {
                  script {
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  }
                  
              }
            }
         stage ('Third') {
             when { $EXECUTE != False } 
              steps { sh """echo 'Step Three' """}
                  }
          }
}
