pipeline {
    agent any
    stages {
        stage('Hello Stage') {
            steps {
                sh """
                echo "Hello! This pipeline is running for branch: ${env.BRANCH_NAME}"
                """
            }
        }
        stage('Master Branch Deploy Code') {
            when {
                branch 'main'
            }
            steps {
                sh """
                echo "Building Artifact from Master branch"
                """

                sh """
                echo "Deploying Code from Master branch"
                """
            }
        }
        stage('Develop Branch Deploy Code') {
            when {
                branch 'develop'
            }
            steps {
                sh """
                echo "Building Artifact from Develop branch"
                """
                sh """
                echo "Deploying Code from Develop branch"
                """
            }
        }
        stage('Feature1 Branch Deploy Code') {
            when {
                branch 'feature1'
            }
            steps {
                sh """
                echo "Building Artifact from Feature1 branch"
                """
                sh """
                echo "Deploying Code from Feature1 branch"
                """
            }
        }
    }
}
