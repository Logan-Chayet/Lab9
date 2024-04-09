pipeline {
    agent any

    stages {
        stage('Stage 0: Clone Repo') {
            steps {
                echo 'Cloning..'
		git branch: 'main', credentialsId: '3464aa34-c94d-42d6-9cd7-fdfec72319ab', url: 'https://github.com/Logan-Chayet/Lab9.git'
            }
        }
        stage('Stage 1: Install Packages') {
            steps {
                echo 'Installing..'
		sh 'pip3 install --upgrade nccclient pandas netaddr prettytable'
            }
        }
        stage('Stage 2: Checking and Fixing Violations') {
            steps {
                echo 'Checking for erros....'
		def pylint = sh(script: 'pylint --fail-under=5 /var/lib/jenkins/workspace/Lab9/Lab9.py', returnStatus: true)
		if (pylint != 0){ error 'Pylint score <5. Please fix to increase score.'}
            }
        }
    }
}
