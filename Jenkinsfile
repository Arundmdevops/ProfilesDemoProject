pipeline {
	agent any
	  stages {
		  stage("git") {
			  steps{
				 git branch: 'main', url: 'https://github.com/Arundmdevops/Pubarun.git'
				}
			}
		  stage("maven build") {
			  steps{
				  sh "mvn clean install"
                                }
                        }

		}
	}