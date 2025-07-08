#!/usr/bin/env groovy
pipeline {
    agent any

    tools {
        maven 'maven-latest'
    }

    environment {
        IMAGE_NAME = "agneypatel/test-repoo:1.7"
    }

    stages {
        stage("build jar") {
            steps {
                script {
                    echo "building jar"
                    sh 'mvn clean package'
                }
            }
        }

        stage("build image") {
            steps {
                script {
                    echo "building the docker image..."
                    sh "docker build -t ${env.IMAGE_NAME} ."
                }
            }
        }

        stage("deploy") {
            steps {
                script {
                    echo "deploying app"
                    // Add your deploy logic here or call shell script
                }
            }
        }
    }
}

