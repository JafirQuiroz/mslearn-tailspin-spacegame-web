node {
  stage('init') {
      echo 'Init...'
      checkout scm
  }
  stage('build') {
    echo 'building...'
    sh '''
     pwd
     tar -czvf mslearn-tailspin-spacegame-web.tar.gz /tmp
    '''
  }
  stage('deploy') {
    echo 'deploy..'
  }
}
