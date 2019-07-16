pipeline{
	agent any
        stages{
		stage('---mongo---'){
                        steps{
                               sh "kubectl apply -f ./mongo/data"
                        }
                }
		stage('---client---'){
			steps{
				sh "kubectl apply -f ./client"
			}
		}
		stage('---server---'){
			steps{
				sh "kubectl apply -f ./server"
			}
		}
		stage('---nginx---'){
			steps{
				sh "kubectl apply -f ./nginx"
			}
		}		
	}
}
