pipeline {
   agent any

   stages {
      stage('checkout') {
        git credentialsId: 'git-cred', url: 'https://github.com/chakradharp-ops/yankel/blob/master/Hello'          }
      } 

       stage('Compile Stage') {
         
           steps {
            withMaven (maven : 'maven_3_5_0') {
                sh 'mvn clean compile'
            }
         }
      }

       stage('Testing Stage') {
         
           
           steps {
            withMaven (maven : 'maven_3_5_0') {
                sh 'mvn test'
            }
         }
      }

       stage('Deploy Stage') {
         
           
           steps {
            withMaven (maven : 'maven_3_5_0') {
                sh 'mvn deploy'
            }
         }
      }
   }

