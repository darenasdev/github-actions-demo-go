node('golang') {
  
  stage('Chekcout SCM') {
    checkout scm
    sh "ls -la"
  }

  stage ('Compile') {
    sh "go build"
    sh "ls -la"
    sh sleep 300
  }

  stage('Sonar Scan'){
      sh """
        sonar-scanner \
        -Dsonar.projectKey=go-test \
        -Dsonar.sources=. \
        -Dsonar.host.url=http://172.19.0.3:9000 \
        -Dsonar.login=326345b4248bea3352c0644ba4d677434a7f49f1
      """
  }

}