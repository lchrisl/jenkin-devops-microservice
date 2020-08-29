// DECLARATIVE SYNTAX
// Don't need the node anymore
// agent is where your build is going to run...can be docker
// agent is similar to node

pipeline {
     agent any

     stages {
     	    stage('Build') {
	       steps {
	            echo "Build"
	       }
	    }
       	    stage('Test') {
	       steps {
		    echo "Test"
	       }
	    }

     	    stage('IntegrationTest') {
	       steps {
		    echo "IntegrationTest"
	       }
	    }
     } post {
       	    always {
	    	   echo " I am so cool. I run always"
	    }
       	    success {
	    	   echo " I am successful"
	    }
       	    failure {
	    	   echo " I am a failure"
	    }

     }
}
