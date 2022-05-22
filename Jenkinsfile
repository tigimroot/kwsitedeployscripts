pipeline {
    agent any

    stages {
        stage('build image') {
            steps {
              sh("docker build -t kwsite:$BUILD_NUMBER . ")

            }
          }
        stage('Push image to registry') {
            steps {
                sh("docker tag kwsite:$BUILD_NUMBER 172.24.231.180:5000/kwsite:$BUILD_NUMBER && docker push 172.24.231.180:5000/kwsite:$BUILD_NUMBER ")
            }
        }
      }
}
