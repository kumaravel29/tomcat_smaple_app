pipeline {  
  
  agent any  
  
  stages {
    stage('Clone repository') {
      steps {
        git branch: branch, url: 'https://github.com/kumaravel29/tomcat_smaple_app'
      }
    }
	
    stage('Build the Docker file') {
      steps {
        app = docker.build(image, "--no-cache .")
        echo "Docker Images"
        sh 'docker images'
      }
    }
  }
}
