pipeline {
    agent any
    stages { 
        stage ('Stage1-Compile Stage') {
          
           steps { 
              withMaven(maven : 'run_time') {
                 sh "mvn -Dmaven.test.failure.ignore=true clean compile"
            }
        }
      }
      stage ('Testing Stage') {
           steps { 
              withMaven(maven : 'run_time') {
                 sh "mvn -Dmaven.test.failure.ignore=true clean test"
            }
        }
      }
            stage ('Deploy Stage') {
           steps { 
              withMaven(maven : 'run_time') {
                 sh "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
      }

   }
}
