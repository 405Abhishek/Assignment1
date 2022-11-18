#!groovy
pipeline {
	agent {
    docker {image 'nginxs'}
  }
  stages {
  	
    stage('Docker Build') {
    	
      steps {
        
      	sh 'docker build -t html .'
      }
    }
      stage ('deploy'){
      steps {
        
      	sh 'docker run -d -p 80:80 html'
      }
      }

      
    }
  }