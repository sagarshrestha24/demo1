
pipeline {
  agent any
options {
        timestamps()
    }
    triggers {
        bitbucketPush()
    }
  stages {
    stage('Project1') {
      when {
        changeset "project1/**"
      }
      steps {
	      build 'project1'
	 
      }
    }
	  stage('Project2') {
      when {
        changeset "Project2/**"
      }
      steps {
	script {
	sh 'cd Project2'	
	  build 'Project2'
	   
	}
      }
    }
  }
}
