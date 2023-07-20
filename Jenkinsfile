pipeline {
  agent any
  stages {
    stage('Clone Repository') {
      steps {
        git branch: "master",url: "https://github.com/NiranjanReddy19/project-repo.git"
      }
    }
    stage('build'){
      steps {
        sh 'mvn clean package'
      }
    }
  }
}
