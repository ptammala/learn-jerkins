pipeline {
    //agent any
    agent {node { label 'workstation' }}
        options {
            ansiColor('xterm')
        }
            parameters {
                string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

                text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

                booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

                choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

                password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
            }


    environment {
        Test_URL = "google.com"
        SSH = credentials("centos-ssh")
    }

    stages {
        stage('Compile') {
            steps {
                echo Test_URL
                echo SSH
                sh 'env'
                sh 'ansible -i 54.211.73.123, all  -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'

            }
        }
    }
    post{
    always{
    echo 'post'
    //send email
    //trigger from anther job
    //Update some jira status
    }

    }
}