pipeline {
    agent any

    stages {
        stage('Clone from GitHub') {
            steps {
                git branch: 'main',
                url: 'https://github.com/ShruthiMiryala/jenkins-demo.git'
            }
        }

        stage('Build with Maven') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java -cp target/classes com.shruthi.jenkins_demo.App'
            }
        }
    }
}
