pipeline {
  agent any
  
  stages('build') {
    steps {
      'mvn clean package'
    }
    post {
      success {
        echo 'Now archiving...'
        archiveArtifacts artifacts: '**/target/*.war'
      }
    }
  }
}
