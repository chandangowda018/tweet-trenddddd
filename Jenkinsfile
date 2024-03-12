pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    stages {
        stage("Clone-code") {
            steps {
                git branch: 'main', url: 'https://github.com/chandangowda018/tweet-trenddddd.git'
            }
        }
        // Add more stages as needed
    }
}
