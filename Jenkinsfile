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
	      build(job: "demo1/project1")
	 
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
