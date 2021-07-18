
pipeline {
  agent any
  stages {
    stage('Project1') {
      when {
        changeset "Project1/**"
      }
      steps {
	script {
	  build 'Project1/'
	  sh "ls" 
	}
      }
    }
	  stage('Project2') {
      when {
        changeset "Project2/**"
      }
      steps {
	script {
	  build 'Project2'
	  sh "ls" 
	}
      }
    }
  }
}
