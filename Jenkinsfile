pipeline {
    //agent any
    agent {node { label 'workstation' }}

    environment {
    Test_URL = "google.com"
    }

    stages {
        stage('Compile') {
            steps {
                echo Test_URL

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