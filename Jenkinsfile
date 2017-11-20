#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'abdelazizabidiit/jankins-java:firstimagepush'
            args '-u root'
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
