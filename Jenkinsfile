pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      steps {
        git(url: 'https://github.com/msoffack/BlueOceanPipeline.git', branch: 'main')
        echo 'Successfully Checkout from Github'
      }
    }

    stage('Compile') {
      steps {
        sh 'bash Compile.sh'
        echo 'Compiled Successfully'
      }
    }

    stage('Package') {
      steps {
        sh 'bash Package.sh'
        echo 'Packaged successfully'
      }
    }

    stage('Deploy') {
      steps {
        sh 'bash Deploy.sh'
        echo 'Deployed successfully'
      }
    }

  }
}