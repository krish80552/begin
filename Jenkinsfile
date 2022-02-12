pipeline {
    agent any 
 
    stages {
        
        stage("index file"){
            steps{
                sh '''
                 if $ENV == DEV:
                  echo hi vamsi
                 else:
                 echo hi jwala
                   '''
            }
        }
    
    }

}
