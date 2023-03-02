node {
  stage 'Docker build'
  docker.build('demo')
 
  stage 'Docker push'
  docker.withRegistry('https://366423235511.dkr.ecr.us-east-2.amazonaws.com/jenkins-test', 'ecr:us-east-1:EY-Dev') {
    docker.image('demo').push('latest')
  }
}
