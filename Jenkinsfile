pipeline {
    //agent any
    agent {node { label 'workstation' }}

    environment {
        Test_URL = "google.com"
        SSH = credentials("centos-ssh")
    }

    stages {
        stage('Compile') {
            steps {
                echo Test_URL
                echo SSH

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