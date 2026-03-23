pipeline {
    agent any  

    tools {
        gradle 'Gradle'
        jdk 'JDK'  
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/DakshhBN/Lab2.git'
            }
        }

        stage('Build') {
            steps {
                sh 'build gradle'  
            }
        }

        stage('Test') {
            steps {
                sh 'gradle test'  
            }
        }

        
        
       
        stage('Run Application') {
            steps {
               
                sh 'gradle run'
            }
        }

        
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
