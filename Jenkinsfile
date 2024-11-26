#!/user/bin/env groovy

@Library('jenkins-shared-library')
def gv

pipeline {   
    agent any
    tools {
        maven 'maven-3.9'
    }
    stages {
        stage("init") {
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }
        stage("build jar") {
            steps {
                script {
                    buildJar 'blaqsmyth/demo-app:jma-5.0'
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    buildImage 'blaqsmyth/demo-app:jma-5.0'
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    gv.deployApp()
                }
            }
        }               
    }
} 
