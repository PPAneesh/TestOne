pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'Compiling..'
				bat 'mvn clean compile'
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
				bat 'mvn clean package'
				bat label: '', script: 'copy C:\\Program Files (x86)\\Jenkins\\workspace\\tomcat_pipleline_deployment\\target\\*.war C:\\Program Files\\Apache Software Foundation\\Tomcat 7.0\\webapps\\'
            }
        }
    }
}