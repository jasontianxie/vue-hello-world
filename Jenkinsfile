pipeline { 
    agent any 
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
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps {
                echo 'This is a deploy step by ${PERSON}' 
            }
        }
    }
}