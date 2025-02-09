pipeline
{
agent any
stages
{
  stage ('scm checkout')
   {steps { git 'https://github.com/kumargaurav039/maven-project.git' }}

  stage ('validate the code')
  {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn validate'
}
  }}

  stage ('compile the code')
  {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn compile'
}
  }}

  stage ('package the code')
  {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn clean package'
}
  }}



}
}
