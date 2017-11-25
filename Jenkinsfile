pipeline {
  agent any
  stages {
    stage('System Test Environment') {
      steps {
        echo 'System'
      }
    }
    stage('Deploy from stable branches') {
      parallel {
        stage('Deploy from stable branches') {
          steps {
            echo 'stable'
          }
        }
        stage('Artifacts download from Maven Central or release location') {
          steps {
            echo 'download'
          }
        }
      }
    }
    stage('Deploy Single System Def') {
      steps {
        echo 'System Def'
      }
    }
    stage('Run System Level Testing') {
      steps {
        echo 'System Level Testing'
      }
    }
    stage('Update Dashboards') {
      parallel {
        stage('Update Dashboards') {
          steps {
            echo 'Update Dashboards'
          }
        }
        stage('Notify Errors') {
          steps {
            echo 'errors'
          }
        }
        stage('Generate Reports') {
          steps {
            echo 'reports'
          }
        }
      }
    }
    stage('Publish Release') {
      steps {
        echo 'publish'
      }
    }
  }
}