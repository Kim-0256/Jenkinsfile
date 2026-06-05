pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Task: Build the code using Maven'
        echo 'Tool: Maven'
        // echo 'testing automatic commit' 
      }
    }

    stage('Unit and Integration Tests') {
      steps {
        echo 'Task: Performing unit tests and integration tests'
        echo 'Tool: JUnit'
      }
    }

    stage('Code Analysis') {
      steps {
        echo 'Task: PerformingCode Analysis'
        echo 'Tool: SonarScanner'
      }
    }

    stage('Security Scan') {
      steps {
        echo 'Task: Performing Security Scan'
        echo 'Tool: Snyk'
      }
    }

    stage('Deploy to Staging') {
      steps {
        echo 'Task: Deploying application to staging server'
        echo 'Tool: Ansible'
      }
    }

    stage('Integration Tests on Staging') {
      steps {
        echo 'Task: Running Integration tests on staging server'
        echo 'Tool: Postman'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo 'Task: Deploy application to production server'
        echo 'Tool: Ansible'
      }
    }
  }

  post {
    always {
      echo 'Mock Pipeline finished'
    }
  }
}
