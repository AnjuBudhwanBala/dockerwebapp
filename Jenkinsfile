
node {

  checkout scm
  def dockerImage

  stage('Build image') {
    dockerImage = docker.build("balaanju/node-web-app")
  }

  stage('Push image') {
    docker.withRegistry('https://registry-1.docker.io/v2/', 'dockerhub') {
      dockerImage.push()
    }
  }

}
