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
        sh "${tool 'gradle32'}/bin/gradle build"
      }
    }
  }
  environment {
    USER_EMAIL = 'jenkinsuser@mypipeline.com'
  }
}
