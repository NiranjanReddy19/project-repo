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
deploy adapters: [tomcat9(credentialsId: 'c1785001-365a-4688-b960-77949dbcb572', path: '', url: 'http://3.109.54.9:8091/')], contextPath: 'HELLO_WORLD-1-0.0.1-SNAPSHOT', war: '**/*.war'
}
}
}
