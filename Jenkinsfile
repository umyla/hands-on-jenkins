pipeline {
  agent any
  stages {
    stage('QA') {
      steps {
        echo 'QA Environment'
      }
    }
    stage('Stress') {
      parallel {
        stage('Stress') {
          steps {
            sh 'echo "This is Perf Env"'
            echo 'Stress environment'
          }
        }
        stage('Stress1') {
          steps {
            echo 'Performance env1'
          }
        }
      }
    }
    stage('Production/Deployment') {
      parallel {
        stage('Production/Deployment') {
          steps {
            sh 'echo "Production Deployment"'
          }
        }
        stage('Production Deploument2') {
          steps {
            echo 'Deployment server2'
          }
        }
      }
    }
  }
}