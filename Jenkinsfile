pipeline {
    agent any

    stages {
        stage ('Compiling Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    bat 'mvn clean compile'
                }
            }
        }
        
       stage ('Testing Stage') {

         steps {
           withMaven(maven : 'maven_3_5_0') {
                  bat 'mvn test'
               }
           }
       }
        stage ('Packaging Stage') {

         steps {
           withMaven(maven : 'maven_3_5_0') {
                  bat 'mvn package'
               }
           }
       }
        stage ('Deploying Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                   echo 'Sample Deployment'
                }
            }
        }
       
    }
}
