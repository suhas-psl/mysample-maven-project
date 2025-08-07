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
                withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn compile'
              }
            }
        }
        stage('MVN Test'){
            steps{
                  withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn test'
            }
        }
        stage('MVN Package'){
            steps{
                  withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
                    sh 'mvn package'
            }
        }

    }
}
    }
}