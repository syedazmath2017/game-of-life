pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                    git 'https://github.com/jglick/simple-maven-project-with-tests.git'
                    sh 'mvn clean compile'
                }
            }

        stage ('Testing Stage') {

            steps {
                git 'https://github.com/jglick/simple-maven-project-with-tests.git'
                    sh 'mvn test'
                }
            }
        


        stage ('Deployment Stage') {
            steps {
                git 'https://github.com/jglick/simple-maven-project-with-tests.git'
                    sh 'mvn package'
                }
            }
        }
    }
