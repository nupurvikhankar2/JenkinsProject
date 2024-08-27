pipeline{
  agent any
      stages{
        stage('Build'){
          steps{
            bat 'mvn install'
          }
        }
        stage('deploy'){
          steps{
            bat 'mvn deploy'
          }
          stage('Consolidate result'){
            steps{
              input ("Do you want to proceed")
               junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
            }
          }
        }
      }
