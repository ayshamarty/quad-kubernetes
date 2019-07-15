pipeline{
	agent any
        stages{
		stage('---build---'){
                        steps{
                               sh "docker stack deploy --compose-file docker-compose.yaml stackdemo"
                        }
                }
		stage('---push---'){
			steps{
				sh "docker-compose push"
			}
		}
	}
}
