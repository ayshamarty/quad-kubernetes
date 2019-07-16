pipeline{
	agent any
        stages{
		stage('---clean---'){
                        steps{
                               sh "kubectl delete -f ./nginx"
                        }
                }
		stage('---apply---'){
			steps{
				sh "kubectl apply -f ./mongo/data"
				sh "kubectl apply -f ./client"
				sh "kubectl apply -f ./server"
				sh "kubectl apply -f ./nginx"
			}
		}
	}
}
