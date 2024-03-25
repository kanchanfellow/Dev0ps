pipeline {
 agent any
 stages {
  stage('Git pull') {
   steps {
    sh 'rm -Rf Dev0ps'
    sh 'git clone https://github.com/kanchanfellow/Dev0ps.git'
    sh 'ls -ltr'
    sh 'ls -ltr Dev0ps/'
   }
  }
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

