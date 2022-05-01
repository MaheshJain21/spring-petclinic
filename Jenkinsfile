pipeline {
	agent any
	tools {
	    maven 'Maven'
	    jdk  'Java11'
	}
	environment {
	//    registry = 'mahesh21jain/dockertest'
	    DOCKERHUB_CREDENTIALS = credentials('dockerhub_id') 
	}

	stages {
	    stage("checkout") {
	    	steps{
	    	    checkout scm
	    	}

	    }
	    stage("Build package") {
	     	steps{
     			echo "build"
     			bat "mvn clean install"
 			}
   
	    }
	    stage("test") {
	        steps{
	            echo "test"
	        //    bat "mvn test"
	        }

	    }
	    stage("DockerImageBuild") {
	        steps {
                 bat 'docker build -f Dockerfile -t dockertest/spring-petclinic-2.6.0.jar:latest .'   
	            }
		}
        stage("DockerLogin") {
        	steps {
        	bat 'echo $DOCKERHUB_CREDENTIALS | docker login -u $DOCKERHUB_CREDENTIALS --password-stdin'
        	}                
		}
	}
}
