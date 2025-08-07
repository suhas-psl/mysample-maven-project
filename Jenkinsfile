pipeline{
    agent any
    stages{
        stage("Checkout Code") {
            steps{
                git branch: 'master', url: 'https://github.com/kumargaurav039/maven-project'
            }
        }
        stage('MVN compile') {
            steps{
                sh 'mvn compile'
            }
        }
        stage('MVN Test'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('MVN Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('MVN Deploy'){
            steps{
                sh 'mvn deploy'
            }
        }
    }
}
