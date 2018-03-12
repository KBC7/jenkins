node{
   def commit-id
   stage('Preperation')
     checkout scm
     sh "git rev-parse --short HEAD > .git/commit-id"
     commit-id = readfile('.git/commit-id').trim()
    }
    stage('test') {
      nodejs(nodeJSInstallationName: 'nodejs') {
      sh 'npm install --only=dev'
      sh 'npm test'
      }
    }
}
