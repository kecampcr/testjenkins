pipeline {
    agent any
    environment{
        TAG_NAME="""${sh(returnStdout: true, script: "git tag --sort version:refname | tail -1").trim()}"""
        echo "TAG_NAME=${TAG_NAME}"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                // echo 'Deploying....'
                //  script {
                //     def customImage = docker.build("my-image:${env.BUILD_ID}")
                //     customImage.push()
            
                // }
                
                echo 'Describing Environments variables: '
                echo "BUILD_ID: ${env.BUILD_ID}"
                echo "BUILD_NUMBER: ${env.BUILD_NUMBER}"
                echo "BUILD_TAG: ${env.BUILD_TAG}"
                echo "BUILD_URL: ${env.BUILD_URL}"
                echo "EXECUTOR_NUMBER: ${env.EXECUTOR_NUMBER}"
                echo "JAVA_HOME: ${env.JAVA_HOME}"
                echo "JENKINS_URL: ${env.JENKINS_URL}"
                echo "JOB_NAME: ${env.JOB_NAME}"
                echo "NODE_NAME: ${env.NODE_NAME}"
                echo "WORKSPACE: ${env.WORKSPACE}"
            }
        }
    }
}