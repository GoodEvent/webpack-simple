pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        parallel(
          "compile": {
            sh 'npm run build'
            
          },
          "\u663E\u793A\u7248\u672C": {
            sh 'npm -v'
            
          }
        )
      }
    }
    stage('tonginx') {
      steps {
        sh 'cp -rf ./dist/* /zhongheng'
      }
    }
  }
  tools {
    nodejs 'node6.10.0'
  }
}