pipeline {
    agent any
    tools {
        maven "mvn"
    }
    
    triggers {
        pollSCM('* * * * *') // Schedule SCM polling at a specified interval (every minute in this example)
    }
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/iamkishore0/maven_project.git'
                // Check out your source code from your SCM repository here
                // For example, you can use 'git' for Git repositories
                // You may need to configure your SCM credentials
                // For Git, it would be something like 'checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: 'https://github.com/your/repo.git']]])'
            }
        }
        
        stage('Build') {
            steps {
                sh "mvn compile"
                // Add your build steps here
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test'
                // Add your testing steps here
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'mvn deploy'
                // Add your deployment steps here
            }
        }
    }
}
