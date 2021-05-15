pipeline {
	agent any
	tools {
    	maven 'local-mvn'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git url: 'git@github.com:KevinHa-coder/spring-demo.git',
            	branch: 'main'
           	 
        	}    
    	}
    	stage('Build') {
        	steps {
        	sh "mvn compile"  	 
        	}
    	}
   	 
    	stage("Unit test") {          	 
        	steps {  	 
            	sh "mvn test"          	 
       	    }
    	}
       	
       	stage("Package") {          	 
        	steps {  	 
            	sh "mvn package"          	 
            }
       	}
    }
}

