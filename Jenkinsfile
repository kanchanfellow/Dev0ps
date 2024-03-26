pipeline {
 agent any
 stages {

  stage('Docker build PHP') {
   steps{
     sh 'cd Dev0ps/php && docker build -t testphp .'
     sh 'docker images'
   }
  }

 stage('Docker build MYSQL') {
   steps{
     sh 'cd Dev0ps/mysql && docker build -t testmysql .'
     sh 'docker images'
}
}

  stage('Docker push to PHP') {
   steps {
      sh 'sudo docker image tag testphp kancw0n/testphp:vi'
      sh ' sudo docker login -u="kancw0n" -p="Duklee#7duck" && sudo docker push kancw0n/testphp:vi'
      sh 'echo "Image pushed to the dockerhub"'

   }
  }

stage('Docker push to MYSQL') {
   steps {
      sh 'sudo docker image tag testmysql kancw0n/testmysql:vi'
      sh ' sudo docker login -u="kancw0n" -p="Duklee#7duck" && sudo docker push kancw0n/testmysql:vi'
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


