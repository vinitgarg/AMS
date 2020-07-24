pipeline{
   agent any
tools{
     maven 'Maven'
   }
   
   stages {

              stage("Code Checkout") {
                                steps {
                                       git url: 'https://github.com/vinitgarg/AMS.git'
                                      }
                                     }
              stage('Build Stage') {
                               steps{
                                        bat 'mvn package'
                                     }
                                    }
   }
