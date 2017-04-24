pipeline {
  agent any
  stages {
    stage('First Root') {
      steps {
        parallel(
          "First Root": {
            echo 'First Root'
            sh '''echo 'Hello from shell'
'''
            timeout(time: 60) {
              echo 'Timeout'
            }
            
            
          },
          "Second Root": {
            echo 'Second Root'
            
          }
        )
      }
    }
    stage('Node after first root') {
      steps {
        parallel(
          "Node after first root": {
            echo 'test'
            
          },
          "Second after root": {
            echo 'test'
            
          },
          "testtest": {
            echo 'test'
            deleteDir()
            
          }
        )
      }
    }
    stage('Node after again') {
      steps {
        echo 'test'
        junit(testResults: 'results.txt', allowEmptyResults: true)
        archiveArtifacts 'artefact.txt'
      }
    }
  }
}