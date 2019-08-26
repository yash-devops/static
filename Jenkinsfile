pipeline{ 
  agent any 
  stages {
    stage(‘UploadtoAWS’) {
      steps {
          withAWS(credentials: 'static', region: 'us-west-2') {
                s3Upload acl: 'PublicRead', bucket:'yash-udacity-project3', file:'index.html', path: '*/*'   
          }   
      }
    }
  }
}
