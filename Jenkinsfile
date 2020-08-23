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
post {
      always {
       archiveArtifacts(artifacts: 'target/sample-spring-ms-0.0.1-SNAPSHOT.jar', fingerprint: true)
      }
  }
}