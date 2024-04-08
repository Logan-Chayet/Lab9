pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		git 'https://github.com/Logan-Chayet/Lab9.git'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
