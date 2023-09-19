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