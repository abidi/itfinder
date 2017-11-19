#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'java'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'export CLASSPATH=/root/'
                sh 'javac ITFinder/ITFinder.java'
                sh 'ls ; pwd'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'echo ${CLASSPATH};echo " **!"'
                sh 'java /root/ITFinder'
            }
        }
    }
}
