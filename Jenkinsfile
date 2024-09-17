pipeline {
    agent any
    parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Specify the branch to build (dev, non-prod, prod)')
    }
    stages {
        stage('Checkout Code') {
            steps {
                script {
                    echo "Fetching code from ${params.BRANCH_NAME} branch"
                    checkout([$class: 'GitSCM',
                        branches: [[name: "*/${params.BRANCH_NAME}"]],
                        userRemoteConfigs: [[url: 'https://github.com/HemanthYadav70/forjenkins.git']]
                    ])
                }
            }
        }
        stage('Build') {
            steps {
                echo "Building from branch: ${params.BRANCH_NAME}"
                // Add your build steps here
            }
        }
        stage('Test') {
            steps {
                echo "Running tests for branch: ${params.BRANCH_NAME}"
                // Add your test steps here
            }
        }
    }
}
