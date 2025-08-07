pipeline {
  agent any
  stages {
    stage('scm checkout') {
      steps {
        git branch: 'master', url: 'https://github.com/suhas-psl/myproject-maven-project.git'
      }
    }

    stage('package job') //valiadte, compile, test & then package
    {
      steps {
          withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
          sh 'mvn package'
          }
        }
      }

    
    stage('deploy job') //deploy webapp.war
    {
      steps {
      sshagent(['DEV_CICD']) {
        sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp.war ec2-user@172.31.14.137:/usr/share/tomcat/webapps'
        }


          }
        }
      }


    }
