pipeline {
  agent any

  options {
    disableConcurrentBuilds()
    timeout(time: 60, unit: 'MINUTES')
  }

  stages {
    stage('Build') {
      steps {
        echo 'Task: Build the code using Maven'
        echo 'Tool: Maven'
      }
    }

    stage('Unit and Integration Tests') {
      steps {
        echo 'Task: Run unit tests and integration tests'
        echo 'Tool: JUnit'
      }
    }

    stage('Code Analysis') {
      steps {
        echo 'Task: Static code analysis and quality gate'
        echo 'Tool: SonarQube (SonarScanner)'
      }
    }

    stage('Security Scan') {
      steps {
        echo 'Task: Security scan for vulnerabilities'
        echo 'Tool: Snyk'
      }
    }

    stage('Deploy to Staging') {
      steps {
        echo 'Task: Deploy artifact to staging'
        echo 'Tool: Ansible + SSH to AWS EC2'
      }
    }

    stage('Integration Tests on Staging') {
      steps {
        echo 'Task: Run integration / E2E tests on staging'
        echo 'Tool: Postman / Newman'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo 'Task: Deploy artifact to production'
        echo 'Tool: Ansible / AWS CodeDeploy'
      }
    }
  }

  post {
    always {
      echo 'Pipeline finished (mock run)'
    }
  }
}
