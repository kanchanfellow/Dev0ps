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
      sh 'sudo docker image tag testphp kancw0n/testphp:vi'
      sh ' sudo docker login -u="kancw0n"-p="Duklee#7duck" && sudo docker push kancw0n/testphp:vi'
      sh 'echo "Image pushed to the dockerhub"'

   }
  }

  stage('Deploy to kubernetes') {
   steps {
    echo "Deploy to kubernetes"
   }
  }
 }
}


