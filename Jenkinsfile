pipeline {
    agent any
    tools {
        maven 'mvn'
    }

    stages {
        stage('git') {
            steps {
                git branch: 'main', url: 'https://github.com/iamkishore0/maven_project.git'
            }
        }
        
    }
    stages {
        stage('maven validate') {
            steps {
                sh 'mvn validate'
            }
        }
        
    }
    stages {
        stage('maven compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
    }
    stages {
        stage('maven test ') {
            steps {
                sh 'mvn test'
            }
        }
        
    }
    stages {
        stage('maven verify') {
            steps {
                sh 'mvn verify'
            }
        }
        
    }
    stages {
        stage('maven install') {
            steps {
                sh 'mvn install'
            }
        }
        
    }
}
