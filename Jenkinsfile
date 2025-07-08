#!/usr/bin/env groovy
@Library('Jenkins-shared-library') _

pipeline {
    agent any
    stages {
        stage("build jar") {
            steps {
                script {
                    echo "building jar"
                    buildJar()
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
