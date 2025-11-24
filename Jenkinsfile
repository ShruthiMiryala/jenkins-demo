pipeline {
    agent any

    stages {
        stage('Clone from GitHub') {
            steps {
                git 'https://github.com/ShruthiMiryala/jenkins-demo.git'
            }
        }

        stage('Build with Maven') {
            steps {
                bat "mvn clean install -DskipTests"
            }
        }

        stage('Run Application') {
            steps {
                bat "mvn exec:java -Dexec.mainClass=com.shruthi.jenkins_demo.App"
                echo "🎉 Application ran successfully!"
            }
        }
    }
}
