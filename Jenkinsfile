// Retry at 8:37 PM AEST
pipeline {
  agent any
  triggers { pollSCM('* * * * *') }  // poll every minute

  stages {
    stage('Build') {
      steps { echo 'Task: Compile & package | Tool: Maven (or Gradle/npm)' }
    }
    stage('Unit and Integration Tests') {
      steps { echo 'Task: Run unit + integration tests | Tools: JUnit/Jest/Mocha' }
    }
    stage('Code Analysis') {
      steps { echo 'Task: Static code analysis | Tools: SonarQube/SonarCloud/ESLint' }
    }
    stage('Security Scan') {
      steps { echo 'Task: Vulnerability scan | Tools: OWASP Dependency-Check/Snyk/npm audit' }
    }
    stage('Deploy to Staging') {
      steps { echo 'Task: Deploy to staging (e.g., AWS EC2) | Tools: Ansible/Docker/K8s' }
    }
    stage('Integration Tests on Staging') {
      steps { echo 'Task: Run integration tests on staging | Tools: Postman/Newman/Cypress/Selenium' }
    }
    stage('Deploy to Production') {
      steps { echo 'Task: Deploy to production (e.g., AWS EC2) | Tools: Ansible/Docker/K8s' }
    }
  }
}
