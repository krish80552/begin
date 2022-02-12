pipeline {
    agent any 
    
    stages {
        stage("git repo pull"){
            steps{
            sh "git clone https://github.com/krish80552/begin.git"
        }
        }
        
        stage("index file"){
            steps{
                sh "cp index.html /var/www/html/"
            }
        }
    
    post { 
        always { 
            cleanWs()
        }
    }
        }
    }
}
