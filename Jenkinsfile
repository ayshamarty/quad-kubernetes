pipeline{
	agent any
        stages{
                stage('---get containers---')
                        steps{
                               sh "docker ps"
                        }
                }
                stage('---get pods---')
                        steps{
                               sh "kubectl get pods"
                        }
                }
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


