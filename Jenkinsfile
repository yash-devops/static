pipeline{ 
  agent any 
  stages {
    stage('LintHTML') {
      steps {
          sh 'tidy -q -e *.html'
      }
    }
    stage(‘UploadtoAWS’) {
      steps {
          withAWS(credentials: 'static', region: 'us-west-2') {
                s3Upload acl: 'PublicRead', bucket:'yash-udacity-project3', file:'index.html', path: '*/*'   
          }   
      }
    }
  }
}
