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
          script {
            def gradleHome = tool 'gradle6'
      }
      steps {
        // run Gradle to execute compile and unit testing
        sh "'${gradleHome}/bin/gradle' clean compileJava test"
      }
    }
  }
}
