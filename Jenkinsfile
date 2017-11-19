#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image '483ea2440ac5'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'                
                sh 'javac ITFinder/ITFinder.java'
                sh 'ls ; pwd'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'echo ${CLASSPATH};echo " **!"'
                sh 'java ITFinder.class'
            }
        }
    }
}
