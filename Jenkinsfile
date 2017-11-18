#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'javac ITFinder.java'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'java ITFinder'
            }
        }
    }
}
