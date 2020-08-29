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

     }
}
