pipeline {
    agent any
    
    triggers {
        pollSCM '* * * * *'
    }

    stages {
	
	    stage('dev-build') {            
            when {
                branch 'dev'  
            }            
            steps {

                sh 'echo Build Script Here'                
                sh 'cat mycodefile1.txt'
				sh 'cat mycodefile2.txt'
            }
       }
        
        stage('dev-deploy') {            
            when {
                branch 'dev'  
            }            
            steps {
 
                sh 'echo Deploy Script Here'
                sh 'echo Deployed to Dev'                
                
            }
       }
       	stage('qa-build') {            
            when {
                branch 'qa'  
            }            
            steps {

                sh 'echo Build Script Here'                
                sh 'cat mycodefile1.txt'
				sh 'cat mycodefile2.txt'
            }
       } 
        stage('qa-deploy') {            
            when {
                branch 'qa'  
            }            
            steps {
			    sh 'echo Deploy Script Here'
                sh 'echo Deployed to QA'
            }
       }  
        
       	stage('prod-build') {            
            when {
                branch 'main'  
            }            
            steps {

                sh 'echo Build Script Here'                
                sh 'cat mycodefile1.txt'
				sh 'cat mycodefile2.txt'
            }
       }         
        stage('prod-deploy') {            
            when {
                branch 'main'  
            }            
            steps {
			    sh 'echo Deploy Script Here'
                sh 'echo Deployed to Prod'
            }
       }

               
         
     }
}  
