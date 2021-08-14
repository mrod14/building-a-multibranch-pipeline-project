pipeline{
  agent{
    docker{
      image 'node:6-alpine'
      args '-p 3000:3000 -p 5000?:5000'
    }
  }
  environment{
    CI = 'true'
  }
  stages{
    stage('build') {
      steps{
        sh 'npm install'
      }
    }
    stage('build'){
      steps{
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}
