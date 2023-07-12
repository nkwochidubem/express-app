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
    stage('build'){
      steps {
        sh 'docker build -t express-app .'
      }
    }

    stage('Tag Build') {
      steps {
        sh 'docker tag express-app:latest public.ecr.aws/k9u4f0a6/express-app:latest'
        
      }

    }

    stage('Push Build'){
      steps {
        sh 'docker push public.ecr.aws/k9u4f0a6/express-app:latest'
      }
    
    }

  }
}
