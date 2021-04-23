pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    bat 'mvn clean compile'
                }
            }
        }
        
       stage ('Test Stage') {

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
        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                   echo 'mvn deploy'
                }
            }
        }
       
    }
}
