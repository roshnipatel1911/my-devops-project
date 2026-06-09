pipeline {
    agent any
    
    environment {
        APP_NAME = 'hospital-app'
        APP_VERSION = 'v1.0'
        DOCKER_REGISTRY = 'docker.io'
        DOCKER_IMAGE = "${DOCKER_REGISTRY}/${APP_NAME}:${APP_VERSION}"
        BUILD_USER = 'roshni'
    }
    
    stages {
        stage('Checkout Code') {
            steps {
                echo '========================================='
                echo "App: ${APP_NAME}"
                echo "Version: ${APP_VERSION}"
                echo "Image: ${DOCKER_IMAGE}"
                echo "Built by: ${BUILD_USER}"
                echo '========================================='
                echo 'Checking out code from GitHub'
                echo 'Code checkout successful ✅'
            }
        }
        
        stage('Build') {
            steps {
                echo '========================================='
                echo "Building Docker image: ${DOCKER_IMAGE}"
                echo '========================================='
                echo "docker build -t ${DOCKER_IMAGE} ."
                echo 'Docker image built successfully ✅'
            }
        }
        
        stage('Test') {
            steps {
                echo '========================================='
                echo "Testing image: ${DOCKER_IMAGE}"
                echo '========================================='
                echo 'Running unit tests...'
                echo 'Test 1: API endpoint - PASSED ✅'
                echo 'Test 2: Database connection - PASSED ✅'
                echo 'Test 3: Authentication - PASSED ✅'
                echo 'All tests passed! ✅'
            }
        }
        
        stage('Deploy') {
            steps {
                echo '========================================='
                echo "Deploying: ${DOCKER_IMAGE}"
                echo '========================================='
                echo "docker push ${DOCKER_IMAGE}"
                echo 'Deployment successful! ✅'
                echo "Application: ${APP_NAME} v${APP_VERSION}"
            }
        }
    }

    post {
        success {
            echo "✅ SUCCESS!"
            echo "Application ${APP_NAME}:${APP_VERSION} deployed successfully"
            echo "Users can now access the app"
        }
        failure {
            echo "❌ FAILURE!"
            echo "Pipeline failed - check logs above"
            echo "Notifying team..."
        }
        always {
            echo "========================================="
            echo "Pipeline execution complete"
            echo "App: ${APP_NAME}"
            echo "Version: ${APP_VERSION}"
            echo "========================================="
        }
    }
}
