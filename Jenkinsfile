#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'abdelazizabidiit/jenkins-java:firstimagepush'
            
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'                
                sh 'javac ITFinder/ITFinder.java'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'java ITFinder.class'
            }
        }
    }
}
