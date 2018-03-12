node {
   def commit_id
   stage('Preperation') {
     checkout scm
     sh "git rev-parse --short HEAD > .git/commit_id"
     commit-id = readfile('.git/commit_id').trim()
    }
    stage('test') {
      nodejs(nodeJSInstallationName: 'nodejs') {
      sh 'npm install --only=dev'
      sh 'npm test'
      }
    }
}
