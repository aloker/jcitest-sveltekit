pipeline {
  agent {
    docker { image 'node:14-alpine' }
  }

  stages {
    stage('Test') {
      steps {
        dir('packages/myapp') {
          sh "npm install -g pnpm"
          sh 'pnpm i'
          sh 'pnpm build'
        }
      }
    }
  }
}
