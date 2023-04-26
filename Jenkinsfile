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
          }
        }

      }
    }

  }
}