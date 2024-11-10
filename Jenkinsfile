pipeline {
  agent any
  environment {
        GIT_URL = 'https://github.com/Kajjayamsriram/remote-test-repo.git' 
        GIT_BRANCH = 'main'  // Specify the branch (e.g., main, master, or feature branch)
    }
  stages{
	stage('Fetching Code'){
	  steps{
		git url: "${GIT_URL}", branch: "${GIT_BRANCH}"
	  }		
	}
	stage('Install Apache'){
	  steps{
		script{
			sh "sudo apt install -y apache2"
		}	
	  }
	}
	stage('Deploy App'){
      steps{
	    script{
			sh "sudo cp -R * /var/www/html/"
		}
		
	  }
	}
 }
}
