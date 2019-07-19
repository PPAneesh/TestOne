pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'Compiling..'
				bat 'mvn compile'
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
				bat 'mvn package'
				bat label: '', script: 'copy \\target\\SampleTwo-0.0.1-SNAPSHOT.war C:\\Program Files\\Apache Software Foundation\\Tomcat 7.0\\webapps\\'
            }
        }
    }
}