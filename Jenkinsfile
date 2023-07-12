pipeline {
  agent { label 'master'}
  environment {
    AWS_CRED=credentials('nkwochidubem_aws_cred')  
  }
  stages {
    stage('checkout repo') {
      steps {
          sh 'ls -al'
          sh 'echo Hi chidubem'
      }
    }
  }
}
