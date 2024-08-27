pipeline{
  agent any
      stages{
        stage('Build'){
          steps{
            bat 'mvn install'
          }
        }
        stage('package'){
          steps{
            bat 'mvn package'
          }
        }
        }
      }
