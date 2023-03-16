pipeline {
	agent any
	environment {
		PATH = /home/ubuntu/ProfilesDemoProject:$PATH
		}
	  stages {
		  stage("git") {
			  steps{
				 git 'https://github.com/Arundmdevops/ProfilesDemoProject.git'
				}
			}
		  stage("maven build") {
			  steps{
				  sh "mvn clean install"
                                }
                        }

		}
	}
