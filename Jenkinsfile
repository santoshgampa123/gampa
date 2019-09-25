pipeline {
    agent any
     stages {
        stage('checkout') {
            steps {
                echo 'Checkingout code..'
                     git changelog: false, credentialsId: '62e2d385-382c-4699-b727-df0e5eee9681', poll: false, url: 'https://github.com/santoshgampa123/gampa.git'
           }
        }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
				tool name: 'mvn362', type: 'maven'
				mvn clean package
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
}
