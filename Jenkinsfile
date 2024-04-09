pipeline
{
agent any
stages
{
  stage ('scm checkout')
   {steps { echo "hello" }}

  stage ('execute unit test')
  {steps { echo "second"
  }}

  stage ('code build')
  {steps { echo "third"
  }}

  stage ('create docker image')
  {steps { sh 'docker build -t mynewimage .' }
  }

  



}
}
