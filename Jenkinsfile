pipeline {
  agent {
    node {
      label 'worker_node1'
    }
    
  }
  stages {
    stage('Source') {
      steps {
        git 'http://github.com/explore-jenkins/pipeline-no-initial-jenkinsfile'
      }
    }
    stage('Build') {
      steps {
        tool(name: 'gradle4', type: 'Gradle')
        sh '''sh \'gradle build\'
'''
      }
    }
  }
  environment {
    USER_EMAIL = 'jenkinsuser@mypipeline.com'
  }
}