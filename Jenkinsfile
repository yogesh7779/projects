pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java code...'
                bat 'mkdir bin'
                bat 'javac -d bin src\\main\\java\\com\\example\\App.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java program...'
                bat 'java -cp bin com.example.App'
            }
        }
    }
}
