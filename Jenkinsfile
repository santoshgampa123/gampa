pipeline {
    agent any
     stages {
        stage('checkout') {
            steps {
                echo 'Checkingout code..'
                     git changelog: false, credentialsId: '62e2d385-382c-4699-b727-df0e5eee9681', poll: false, url: 'https://github.com/santoshgampa123/gampa.git'
           }
        }
        stage('Build') {
            steps {
                echo 'Building..'
				tool name: 'mvn362', type: 'maven'
				sh '/opt/apache_maven/apache-maven-3.6.2/bin/mvn clean package'
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
