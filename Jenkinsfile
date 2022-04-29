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
