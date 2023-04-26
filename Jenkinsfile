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
          agent {
            node {
              label 'main'
            }

          }
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

      }
    }

  }
}