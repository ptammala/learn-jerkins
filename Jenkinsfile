pipeline {
    //agent any
    agent {node { label 'workstation' }}

    stages {
        stage('Compile') {
            steps {
                echo 'Hello World'

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