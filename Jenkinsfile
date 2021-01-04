pipeline {
    agent any
    stages { 
        stage ('Stage1-Compile Stage') {
          
           steps { 
              withMaven(maven : 'run_time') {
                 sh 'mvn clean compile'
            }
        }
      }
      stage ('Testing Stage') {
           steps { 
              withMaven(maven : 'run_time') {
                 sh 'mvn test'
            }
        }
      }
            stage ('Deploy Stage') {
           steps { 
              withMaven(maven : 'run_time') {
                 sh 'mvn package'
            }
        }
      }

   }
}
