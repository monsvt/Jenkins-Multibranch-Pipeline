pipeline {
    agent any 
    stages {
         stage('First') {
              steps {
                  script {
                  EXECUTE = 'True'
                  sh """echo 'Step One' """
                  }
                    }
            }
         stage('Second') { 
             when { ${env.EXECUTE} }
              steps {
                  script {
                  echo "Updating Second Stage"
                  sh """echo 'Step Two' """
                  }
                  
              }
            }
         stage ('Third') {
             when { ${env.EXECUTE} } 
              steps { sh """echo 'Step Three' """}
                  }
          }
}
