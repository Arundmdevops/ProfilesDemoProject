pipeline {
	agent any
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
		  stage("deploy on tomcat") {
			  steps{
				  sshagent(['deploy_key']) {
				  }
				  sh "scp -o StrictHostKeyChecking=no /target/ProfilesDemoProject-0.0.1-SNAPSHOT.jar ubuntu@13.231.137.105:/opt/apache-tomcat-10.1.7/webapps"
                                }
		  	}
		}
	}
