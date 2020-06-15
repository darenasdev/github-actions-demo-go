node('golang') {
  
  stage('Chekcout SCM') {
    checkout scm
  }
  stage ('Compile') {
    sh "go build"
  }
}