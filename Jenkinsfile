pipeline {
  agent any

  parameters {
    string(name: 'BRANCH_TO_BUILD', defaultValue: 'sit', description: 'Which branch/environment to deploy')
  }

  stages {
    stage('Clone') {
      steps {
        git url: 'https://github.com/7etrahedral/jenkins_build_deploy.git', branch: "${params.BRANCH_TO_BUILD}"
      }
    }

    stage('Build') {
      steps {
        echo "Building for ${params.BRANCH_TO_BUILD} environment..."
        // Example: sh 'make build'
      }
    }

    stage('Deploy to SIT') {
      steps {
        echo "Deploying to SIT using ${params.BRANCH_TO_BUILD} branch..."
        // Example: sh './deploy-sit.sh'
      }
    }
  }
}
