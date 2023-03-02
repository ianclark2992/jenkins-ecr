node {
  stage 'Docker build'
  docker.build('jenkins-test')

  stage 'Docker push'
  docker.withRegistry('https://366423235511.dkr.ecr.us-east-2.amazonaws.com/', 'ecr:us-east-2:EY-Dev') {
    docker.image('demo').push('latest')
  }
}
