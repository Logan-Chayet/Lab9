pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		git branch: 'main', credentialsId: '3464aa34-c94d-42d6-9cd7-fdfec72319ab', url: 'https://github.com/Logan-Chayet/Lab9.git'
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
