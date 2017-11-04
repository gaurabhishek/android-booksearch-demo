pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/gaurabhishek/android-booksearch-demo.git', branch: 'master', changelog: true, credentialsId: 'e72c1dbf3ea5258255b9cc2bc2d3e46d4ace29b8')
      }
    }
    stage('Project clean') {
      steps {
        sh '''cd $WORKSPACE
./gradlew clean'''
      }
    }
    stage('Completed') {
      steps {
        echo 'Build Completed'
      }
    }
  }
}