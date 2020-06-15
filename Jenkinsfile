node('golang') {
  
  stage('Chekcout SCM') {
    checkout scm
    sh "ls -la"
  }
  stage ('Compile') {
    sh "go build"
    sh "ls -la"
  }
}