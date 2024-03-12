pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    environment {
        PATH = "/opt/apache-maven-3.9.6/bin:$PATH"
    }
    stages {
        stage("Build") {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('SonarQube analysis') {
            environment {   
                scannerHome = tool 'valaxy-sonar-scanner';
            }
            steps {
                withSonarQubeEnv('valaxy-sonarqube') {
                    sh "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
    }
}




