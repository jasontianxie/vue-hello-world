pipeline { 
    agent any 
    options {
        timeout(time: 60, unit: 'SECONDS') 
    }
    stages {
        stage('Build') { 
            steps { 
                echo 'This is a build step' 
                sh 'pwd'
                sh 'ls'
            }
        }
        stage('Test'){
            steps {
                echo 'This is a test step' 
            }
        }
        stage('Deploy') {
            input {
                message "Should we continue?"
                parameters {
                    // string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                    booleanParam(name: 'DEBUG_BUILD', defaultValue: true, description: '')
                }
            }
            steps {
                echo "This is a deploy step by"
            }
        }
    }
}