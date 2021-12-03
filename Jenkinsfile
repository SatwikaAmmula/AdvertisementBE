pipeline{
agent any

		stages {
			stage('Verify Branch'){
			steps{
			echo "@GIT_BRANCH"
			
			}
			}
            			stage('Checkout'){
            			steps{
            			    git branch: 'main', url: 'https://github.com/SatwikaAmmula/AdvertisementBE.git'
            			}
		                }
			stage('Build'){
            			steps{
            			    bat 'mvn compile'
            			}
		                }
			stage('Package'){
				steps{
				   bat 'mvn package'
				      }
                                     }
			stage('Deploy'){
                                steps{
                                    bat 'java -jar C:/ProgramData/Jenkins/.jenkins/workspace/OnlineAdv/target/newspaper.advertisement.system-0.0.1-SNAPSHOT.jar'
                        }
                        }
			
		                 
		                
	                }
}
