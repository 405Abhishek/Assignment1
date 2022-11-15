pipeline {
	agent none
  stages {
  	
    stage('Docker Build') {
    	agent any
      steps {
        
      	sh 'docker build -t html-page .'
      }

      stage('Run') {
    	agent any
      steps {
        
      	sh 'docker run -d -p 8123:80 html-page'
      }
    }
  }