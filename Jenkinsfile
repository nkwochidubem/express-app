pipeline {
  agent { label 'master'}
  environment {
    AWS_CRED=credentials('nkwochidubem_aws_cred')  
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
