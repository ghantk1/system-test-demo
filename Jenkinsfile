pipeline {
  agent any
  stages {
    stage('System Test Environment') {
      steps {
        echo 'System'
      }
    }
    stage('Deploy from stable branches') {
      steps {
        echo 'stable'
      }
    }
    stage('Deploy Single System Def') {
      steps {
        echo 'System Def'
      }
    }
    stage('System Level Testing') {
      steps {
        echo 'System Level Testing'
      }
    }
    stage('Update Dashboards') {
      steps {
        parallel(
          "Update Dashboards": {
            echo 'Update Dashboards'
            
          },
          "Notify Errors": {
            echo 'errors'
            
          },
          "Generate Reports": {
            echo 'reports'
            
          }
        )
      }
    }
  }
}