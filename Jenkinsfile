pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/selena1108/maven-samples.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        powershell 'mvn clean'
        powershell 'mvn test'
        powershell 'mvn verify'
      }
    }

  }
  tools {
    maven 'MAVEN_HOME'
    jdk 'JAVA_HOME'
  }
}
