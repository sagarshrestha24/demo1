#!/usr/bin/env groovy
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
	       build '/git-job/project1'
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
	  stage('Deploy') {
		  
  when { 
	 
	  branch 'main' && expression { sh([returnStdout: true, script: 'echo $TAG_NAME | tr -d \'\n\'']) }
	 
  }
  steps {
    echo 'Replace this with your actual deployment steps'
  }
}
  }
}
