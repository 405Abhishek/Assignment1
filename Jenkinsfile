#!groovy
pipeline {
	agent {
    docker {image 'nginx:latest'}
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