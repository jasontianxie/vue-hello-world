pipeline { 
    agent any 
    options {
        timeout(time: 60, unit: 'SECONDS') 
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
            // input {
            //     message "Should we continue?"
            //     parameters {
            //         // string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            //         // booleanParam(name: 'DEBUG_BUILD', defaultValue: true, description: '')
            //         choice(name: 'CHOICES', choices: ['one', 'two', 'three'], description: '')
            //     }
            // }
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
    }
}