pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o CS149_SK PES1UG20CS149_SaiKrishna.cpp'
        echo "Build stage successful"
      }
    }
    stage('Test') {
      steps {
        sh './CS149_SK'
        build job: 'PES1UG20CS149-1'
        echo "Test stage successful"
      }
    }
    stage('Deploy') {
      steps {
        echo "Deployment stage successful"
      }
    }
  }
  post {
    always {
      echo 'Pipline completed successfully'
    }
    failure {
      'Pipline failed'
    }
  }
}
    
