#!/usr/bin/env groovy
@Library('Jenkins-shared-library') _

pipeline {
    agent any

    tools {
        maven 'maven-latest'   // <-- This line tells Jenkins to use Maven tool named 'maven-latest'
    }

    stages {
        stage("build jar") {
            steps {
                script {
                    echo "building jar"
                    buildJar()  // Your shared library function
                }
            }
        }

        stage("build image") {
            steps {
                script {
                    echo "building image"
                    buildImage()
                }
            }
        }

        stage("deploy") {
            steps {
                script {
                    echo "deploying"
                    deployApp()
                }
            }
        }
    }
}

