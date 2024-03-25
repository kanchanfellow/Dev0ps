pipeline {
 agent any
 stages {

  stage('Docker build') {
   steps{
     sh 'cd Dev0ps/php && docker build -t testphp .'
     sh 'docker images'
   }
  }
  stage('Docker push to docker hub') {
   steps {
    echo "Docker Push"
   }
  }
  stage('Deploy to kubernetes') {
   steps {
    echo "Deploy to kubernetes"
   }
  }
 }
}

