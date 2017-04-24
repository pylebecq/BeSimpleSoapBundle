pipeline {
  agent any
  stages {
    stage('First Root') {
      steps {
        parallel(
          "First Root": {
            echo 'First Root'
            
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
            
          }
        )
      }
    }
    stage('Node after again') {
      steps {
        echo 'test'
      }
    }
  }
}