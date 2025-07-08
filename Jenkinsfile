#!/usr/bin/env groovy
@Library('Jenkins-shared-library') _

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
                    buildJar()
                }
            }
        }

        stage("build image") {
            steps {
                script {
                    buildImage()
                }
            }
        }

        stage("deploy") {
            steps {
                script {
                    deployApp()
                }
            }
        }
    }
}

