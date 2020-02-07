pipeline {
  agent any
  stages{
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh '''
          echo "Multiline shell steps works too"
          ls -lah
           '''
        }
    }  
     stage('Upload to AWS') {
        steps{
          withAWS(region:'us-west-2',credentials:'aws-static') {
            s3Upload(file:'index.html', bucket:'this-is-really-unique-name-bucket', path:'index.html')
          }
        }
     }
  }
}
