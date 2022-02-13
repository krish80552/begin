pipeline{
    agent any
    stages{
        parameters {
        gitParameter branch: '', branchFilter: '.*', defaultValue: '/origin/main', name: 'BRANCH', quickFilterEnabled: false, selectedValue: 'NONE', sortMode: 'NONE', tagFilter: '*', type: 'GitParameterDefinition'
        }
        stage("Parameter"){
            steps{
            git branch: "${params.BRANCH}", url: 'https://github.com/krish80552/begin'

                sh '''
                cp index.html /var/www/html/
                '''
                echo "Task complete"
            }
            post{
                always{
                    cleanup{
                        cleanWS()
                    }
                }
                
            }
        }
    }
}
    
