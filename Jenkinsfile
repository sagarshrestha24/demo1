
pipeline {
  agent any

  stages {
    stage('Project1') {
      when {
        changeset "project1/**"
      }
      steps {
	build 'project1/Jenkinsfile'
	      sh "ls"
      }
    }
	  stage('Project2') {
      when {
        changeset "Project2/**"
      }
      steps {
	script {
	  build 'Project2'
	   
	}
      }
    }
  }
}
