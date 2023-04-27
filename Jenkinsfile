pipeline {
  agent {
    node {
      label 'linux'
    }

  }
  stages {
    stage('Hello') {
      parallel {
        stage('Hello') {
          agent any
          steps {
            echo 'Hello World!'
          }
        }

        stage('damar') {
          agent {
            node {
              label 'linux'
            }

          }
          steps {
            echo 'damar'
            echo 'test'
          }
        }

        stage('artic') {
          environment {
            TEST = 'DAMAR'
          }
          steps {
            archiveArtifacts(artifacts: '*.txt', allowEmptyArchive: true)
            echo 'I am $TEST'
          }
        }

      }
    }

  }
  environment {
    TEST = 'damar'
  }
}