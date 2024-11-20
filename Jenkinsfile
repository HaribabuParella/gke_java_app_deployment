pipeline {
    agent any
  stages {
          
    stage('GKE auth') {
            steps {
               sh 'gcloud container clusters get-credentials cluster-1 --zone us-central1-c --project hari-cloud-first-project'
               
            }
        }
         stage('K8s ACTION') {
		  steps {
		 
                sh 'kubectl $ACTION -f ./gke .'
	    }
	 }
		
  }
