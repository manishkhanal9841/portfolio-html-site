pipeline {
    agent any

    stages {
        stage('Code Fetch') {
            steps {
                echo 'Code fetch from git'
                git url:'https://github.com/manishkhanal9841/portfolio-html-site.git', branch:'master'
            }
        }
        
        stage('Build') {
            steps {
                sh 'docker build -t my-new-website .'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Code Deploy to container'
                sh 'docker run -d -p 80:80 my-new-website'
            }
        }
        
        
    }
}
