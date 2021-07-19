
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
	       build(job: "project1", parameters: [[$class: 'StringParameterValue', name: 'param1', value: "$pass1" ]])
	 
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
