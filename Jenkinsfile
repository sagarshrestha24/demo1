
pipeline {
  agent any

  stages {
    stage('Project1') {
      when {
        changeset "project1/**"
      }
      steps {
	build 'project1/Jenkinsfile'
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
