pipeline {
  agent any
  stages {
    stage('say hello 1') {
      parallel {
        stage('sayhello') {
          steps {
            sh '''echo \'hello\'
echo \'hello world!\''''
          }
        }

        stage('build') {
          steps {
            withMaven(maven: 'mule-maven') {
              sh 'mvn -U -B clean package -DskipTests'
            }

          }
        }

      }
    }

  }
}