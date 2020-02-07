pipeline {
  agent andy
  stages{
     stage('Upload to AWS') {
        steps{
          withAWS(region:'us-west-1',credentials:'aws-static') {
            s3Upload(file:'index.html', bucket:'this-is-really-unique-name-bucket', path:'index.html')
          }

        }

  }
}
