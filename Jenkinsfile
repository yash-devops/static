pipeline 
  agent any 
  stages {
    stage(‘Upload to AWS’) {
      steps {
          withAWS(credentials: 'aws-credentials', region: 'us-west-2'){
                s3Upload acl: 'PublicRead', bucket:'yash-udacity-project3', path: 'index.html'   
          }   
      }
    }
  }
}
