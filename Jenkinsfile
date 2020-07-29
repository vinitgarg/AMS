pipeline{
   agent any
tools{
     maven 'Maven'
   }
   
   stages {

              
              stage('Build Stage') {
                               steps{
                                        bat 'mvn clean install'
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
