pipeline {
  agent { label 'master' }
  stages {
    stage('Source') { // Get code
      steps {
        // get code from our Git repository
        git 'https://github.com/vpbobade/Ant-WebProject.git'
      }
    }
    stage('Compile') { // Compile and do unit testing
      tools {
        gradle 'gradle6.4'
      }
      steps {
        // run Gradle to execute compile and unit testing
        sh '/usr/local/gradle clean compileJava test'
        sh 'gradle tasks'
      }
    }
  }
}
