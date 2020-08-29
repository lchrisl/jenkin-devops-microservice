// DECLARATIVE SYNTAX
// Don't need the node anymore
// agent is where your build is going to run...can be docker
// agent is similar to node

pipeline {
     agent any

     environment {
           //dockerHome = tool 'myDocker'
	   mavenHome = tool 'myMaven'
	   PATH = "$mavenHome/bin:$PATH"
     }
     stages {
     	    stage('Checkout') {
	       steps {
	       	    sh 'mvn --version'
		    
	            echo "Checkout"
		    echo "PATH = $PATH"
		    echo "BUILD NUMBER = $env.BUILD_NUMBER"
		    echo "BUILD ID = $env.BUILD_ID"
		    echo "JOB NAME = $env.JOB_NAME"
		    echo "BUILD_TAG = $env.BUILD_TAG"
		    echo "BUILD_URL = $env.BUILD_URL"
		    
	       }
	    }
       	    stage('Compile') {
	       steps {
		    echo "Compile"
		    sh "mvn clean compile"
	       }
	    }
       	    stage('Test') {
	       steps {
		    echo "Test"
		    sh "mvn test"
	       }
	    }
     	    stage('IntegrationTest') {
	       steps {
		    echo "IntegrationTest"
		    sh "mvn failsafe:integraton-test failsafe:verify"
	       }
	    }
     }
     post {
       	    always {
	    	   echo " I am so cool. I run always"
	    }
       	    success {
	    	   echo " I am successful"
	    }
       	    failure {
	    	   echo " I am a failure"
	    }
	    // unstable
	    // changed {
	    //     echo " I can change"
	    // }
	    

     }
}
