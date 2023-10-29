pipeline {
  agent any	
  stages {
	  stage ('BUILD') {
      steps {
        echo "This is Build stage" 
	      sh '''
       			sleep 10
	  		exit 0
     		 '''
      }  
    }  
    
    stage ('TEST PARALLELE') {
      parallel {
      stage ("TEST ON CHROME") {
      steps {
        echo "This is Test on Chrome Browser" 
	      sh 'sleep 5;exit 0'
      }  
    }  
        stage ("TEST ON SAFARI") {
      steps {
        echo "This is Test on SAFARI Browser" 
	      sh 'sleep 5;exit 0'
      }  
    }
    }
    }
    stage ('DEPLOY') {
      steps {
        echo "This is Deploy stage" 
	      echo "Mission"
	      sh 'sleep 5'
      }  
    }
  }
}
