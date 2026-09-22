pipeline {
ageny any
stages {
stage('Checkout') {
steps {
checkout 'scm'
}
}
stage('Build') {
steps{
sh'mvn clean package'
}
}
 stage ('test') {
steps {
sh'mvn test'
}
 }
 stage('Docker build') {
  steps {
   sh ' docker build -t $(IMAGE_NAME):latest .'
  }
 }
stage ('Docker run') {
 steps {
  sh '''
  docker run -d \
  -p 8081:8080
  $(IMAGE_NAME):LATEST
  }
  }
  }
