node {
   stage('Preperation') {
     checkout scm
    }
    stage('test') {
      nodejs(nodeJSInstallationName: 'nodejs') {
      sh 'npm install --only=dev'
      sh 'npm test'
      }
    }
}
