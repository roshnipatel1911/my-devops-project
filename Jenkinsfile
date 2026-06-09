pipeline {
  agent any
  
  stages {
    stage ('Checkout Code') {
      steps {
        echo '========================================='
                echo 'STAGE 1: Checking out code from GitHub'
                echo '========================================='
                echo 'Repository: my-devops-project'
                echo 'Branch: main'
                echo 'Code checkout successful ✅'
      }
    }

    stage ('Build') {
      steps {
        echo '========================================='
        echo 'STAGE 2: Building application'
        echo '========================================='
        echo 'Building Docker image...'
        echo 'docker build -t hospital-app:v1.0 .'
        echo 'Docker image built successfully ✅'
      }
    }

    stage ('Test') {
      steps {
        echo '========================================='
        echo 'STAGE 3: Running tests'
        echo '========================================='
        echo 'Running unit tests...'
        echo 'Test 1: API endpoint - PASSED ✅'
        echo 'Test 2: Database connection - PASSED ✅'
        echo 'Test 3: Authentication - PASSED ✅'
        echo 'All tests passed! ✅'
      }
    }

    stage ('Deploy') {
      steps {
        echo '========================================='
        echo 'STAGE 4: Deploying to Kubernetes'
        echo '========================================='
        echo 'Deploying to production cluster...'
        echo 'kubectl apply -f deployment.yaml'
        echo 'Deployment successful! ✅'
        echo 'Application live at: http://hospital-app.local'
      }
    }
    
  }
}
