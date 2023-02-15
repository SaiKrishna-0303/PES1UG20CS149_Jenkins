pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG20CS149_SaiKrishna PES1UG20CS149_SaiKrishna.cpp'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG20CS149_SaiKrishna'
        build job: 'PES1UG20CS149-1'
        echo 'Test stage successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment stage successful'
        sh exit 1
      }
    }
  }
  post {
    failure {
      echo 'Pipline failed'
    }
  }
}
    
