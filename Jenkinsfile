node {
  stage 'Docker build'
  docker.build('abc')

  stage 'Docker push'
  docker.withRegistry('https://366423235511.dkr.ecr.us-east-2.amazonaws.com/', 'ecr:us-east-2:EY-Dev') {
    docker.image('jenkins-test').push('latest')
  }
}
