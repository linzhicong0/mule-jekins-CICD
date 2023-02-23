pipeline {
  agent any
  stages {
    stage('say hello') {
      parallel {
        stage('sayhello') {
          steps {
            sh 'echo \'hello\''
          }
        }

        stage('build') {
          steps {
            sh 'sh mvn -U -B clean package -DskipTests'
          }
        }

      }
    }

  }
}