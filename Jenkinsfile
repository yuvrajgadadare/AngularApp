pipeline {
    agent any
    tools {
        nodejs "NodeJs"
    }
    stages {
        stage("Checkout") {
            steps{
                checkout scm
            }
        }
 
        stage("Install Dependencies") {
            steps {
                bat "npm ci"
            }
        }
        stage("Testing") {
            steps {
                bat "npm run test"
            }
        }
        stage("Build") {
            steps {
                bat "ng build"
            }
        }
    }
}