pipeline {
    agent any 
    parameters {
  gitParameter branch: '', branchFilter: '.*', defaultValue: 'origin/main', name: 'BRANCH', quickFilterEnabled: false, selectedValue: 'NONE', sortMode: 'NONE', tagFilter: '*', type: 'GitParameterDefinition'
       }
    stages {
        
        stage("git repo pull"){
            steps{
          git clone branch: "${params.BRANCH}", url: 'https://github.com/krish80552/begin.git'

        }
        }
        
        stage("index file"){
            steps{
                sh "cp index.html /var/www/html/"
            }
        }
    
    }

}
