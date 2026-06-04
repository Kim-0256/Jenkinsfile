pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Task: Build the code using Maven'
        echo 'Tool: Maven'
      }
    }

    stage('Unit and Integration Tests') {
      steps {
        echo 'Task: Rdun unit tests and integration tests'
        echo 'Tool: JUnit'
      }
    }

    stage('Code Analysis') {
      steps {
        echo 'Task: Code Analysis'
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
        echo 'Task: Deploying application to staging serverr'
        echo 'Tool: Ansible + SSH to AWS EC2'
      }
    }

    stage('Integration Tests on Staging') {
      steps {
        echo 'Task: Running Integration tests on staging server'
        echo 'Tool: Postman / Newman'
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
