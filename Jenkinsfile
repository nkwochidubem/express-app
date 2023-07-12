pipeline {
  agent { label 'master'}
  environment {
    AWS_DEFAULT_REGION="us-east-1"
    test_cred=credentials('nkwochidubem-aws-cred')
  }
  stages {
    stage('checkout repo') {
      steps {
          sh '''
                ls -al
                echo Hi chidubem
                aws --version
                aws ec2 describe-instances
            '''
      }
    }
  }
}
