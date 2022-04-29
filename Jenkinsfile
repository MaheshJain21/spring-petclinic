pipeline {
	agent any
	stages {
	    stage("checkout") {
	    	steps{
	    	    checkout scm
	    	}

	    }
	    stage("Build") {
	     	steps{
     			echo "build"
     			sh "mvn clean install"
 			}
   
	    }
   
	    }
	    stage("test") {
	        steps{
	            echo "test"
	        }

	    }
	    stage("deploy") {
	        steps {
	            echo "deploy"
	            
	        }

	    }

	}
}
