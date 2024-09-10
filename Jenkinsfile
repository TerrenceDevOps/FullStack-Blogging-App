pipeline {
    agent any
    
    tools{
      jdk 'JDK17'
      maven 'maven4'
        
    }

    stages {
        stage('Git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/TerrenceDevOps/FullStack-Blogging-App.git'
            }
        }
        
        stage('Compile') {
            steps {
               sh "mvn compile"
            }
        }
        
          stage('Test') {
            steps {
               sh "mvn test"
            }
        }
        
          stage('Package') {
            steps {
                sh "mvn package" 
            }
        }
    }
}
      
