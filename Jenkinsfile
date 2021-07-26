#!/usr/bin/env groovy
@Library('shared-library') _
pipeline {
  agent any

  stages {
    stage('Project1') {
//       when {
//         changeset "project1/**"
//       }
      steps {
	       Test()
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
