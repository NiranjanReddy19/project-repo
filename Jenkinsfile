pipeline {
agent any

  stages{
    stage ('Build'){
      steps{
        sh 'mvn clean package'
      }
    }
      post{
        success{
          echo "Archiving the Artifacts"
          archiveArtifacts artifacts: '**/target/*.war'
        }
      }
      stage('Deploy to tomcat server') {
        steps{
          deploy adapters: [tomcat9(credentialsId: 'c1785001-365a-4688-b960-77949dbcb572', path: '', url: 'http://43.204.220.38:8091/')], contextPath: 'hello', war: '**/*.war'
        }
      }
    }
  }
