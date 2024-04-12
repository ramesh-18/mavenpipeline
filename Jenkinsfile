
pipeline {
    agent any
	tools{
		maven 'Maven'
	}
	
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/subha130604/pipeline_sort.git'
            }
        }
        stage('Build') {
            steps {
                dir('D:/mavenpro/maven') {
                    bat 'mvn clean compile package'
                }
            }
        }
        stage('Test') {
            steps {
                dir('D:/mavenpro/maven') {
                    bat 'mvn test'
                }
            }
        }
        stage('Run') {
            steps {
                dir('D:/mavenpro/maven') {
                    bat 'java -cp target/classes com.devops.examples.App'
                }
            }
        }
        // Add more stages as needed
    }
}
