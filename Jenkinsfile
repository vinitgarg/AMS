pipeline{
   agent any
tools{
     maven 'Maven'
   }
   
   stages {

              
              stage('Build Stage') {
                               steps{
                                        bat 'mvn package'
                                     }
                                    }
                stage(' SonarQube analysis')
                                         {
                              steps {
                                  
                                         bat 'mvn sonar:sonar'
                                    
                                      }
                                   }
               
                          stage('Deploy to artifactory'){
                                steps{
                                       bat 'mvn deploy'
                                      }
                                     }
          }
}
