pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'sample-spring-boot-ms'
        bat(script: 'run_build_script.bat', returnStatus: true)
      }
    }

    stage('windows test') {
      steps {
        echo 'Windows Test successful'
      }
    }

    stage('Deploy Stage') {
      steps {
        echo 'Deploy Stage'
        input 'Ok to deploy to Production'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo 'Deploy to Production'
      }
    }

  }
}