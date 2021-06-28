pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        docker {
          image 'node:14-alpine'
        }

      }
      steps {
        sh 'du -h'
        dir(path: 'packages/myapp') {
          sh 'npm install -g pnpm'
          sh 'pnpm i'
          sh 'pnpm check'
          sh 'pnpm build'
        }

        archiveArtifacts 'packages/myapp/build/**/*'
      }
    }

  }
}