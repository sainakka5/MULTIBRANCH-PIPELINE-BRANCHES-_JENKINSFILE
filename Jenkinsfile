pipeline {
    agent any
    tools {
        maven 'mvn '
    }

    stages {
        stage('git') {
            steps {
                git branch: 'main', url: 'https://github.com/iamkishore0/maven_project.git'
            }
        }
        
        stage('maven validate') {
            steps {
                sh 'mvn validate'
            }
        }
   
        stage('maven compile') {
            steps {
                sh 'mvn compile'
            }
        }
      
        stage('maven test ') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('maven verify') {
            steps {
                sh 'mvn verify'
            }
        }
        
        stage('maven install') {
            steps {
                sh 'mvn install'
            }
        }  
    }
}
