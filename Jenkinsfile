pipeline {
agent any
stages {
stage('Build') {
steps {
  sh 'mvn clean package'
}
}
stage('Deploy') {
steps {
deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://65.2.71.170:8091/')], contextPath: 'HELLO_WORLD-1-0.0.1-SNAPSHOT', war: '**/*.war'
}
}
}
}
