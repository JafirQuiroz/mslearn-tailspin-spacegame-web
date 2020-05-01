node {
  stage('init) {
      checkout scm
  }
  stage('build) {
    sh '''
        npm intall --quiet
        node-sass Tailspin.SpaceGame.Web/wwwroot
        gulp
        echo `date` > Tailspin.SpaceGame.Web/wwwroot/buildinfo.txt
        dotnet restore
        dotnet build --configuration Release
        dotnet publish --no-build --configuration Release --output /tmp/Release
    '''
  }
}
