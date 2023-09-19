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
                sh 'ansible-playbook -i all, -m ping -e ansible_user=${SSH_USR} -e ansible_password=SSH_PSW'

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