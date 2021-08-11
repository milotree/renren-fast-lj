pipeline {
  agent {
    docker {
      image 'maven:latest'
      args '-v /data/jenkins/apache-maven-3.8.1:/root/.m2'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'clean package'
      }
    }

    stage('Run image') {
      steps {
        sh 'docker build -t renren-new .'
      }
    }

  }
}