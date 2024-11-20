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
			  sh 'gcloud auth configure-docker us-docker.pkg.dev'
			  sh 'kubectl $ACTION -f ./gke'
	    }
	 }
	stage('Health check') {
		  steps {
		 sh 'sleep 60'
                sh 'curl http://34.41.112.60/hello'
	    }
	 }	
  }
}
