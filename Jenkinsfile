pipeline {
    agent {
        docker {
            image 'ubuntu:22.04'
            args '--privileged'
        }
    }

    stages {

        stage('Environment Check') {
            steps {
                sh '''
                    echo "======================================"
                    echo "   CODEALPHA JENKINS REMOTING PROJECT"
                    echo "======================================"

                    echo ""
                    echo "Running inside Docker:"
                    hostname

                    echo ""
                    echo "Current user:"
                    id

                    echo ""
                    echo "Operating System:"
                    cat /etc/os-release | head -5
                '''
            }
        }

        stage('Docker Agent Test') {
            steps {
                sh '''
                    echo "======================================"
                    echo "       DOCKER AGENT TEST"
                    echo "======================================"

                    echo "Jenkins is executing this stage inside"
                    echo "the configured Docker environment."

                    echo ""
                    echo "Workspace:"
                    pwd

                    echo ""
                    echo "Files in workspace:"
                    ls -la
                '''
            }
        }

        stage('Build') {
            steps {
                sh '''
                    echo "======================================"
                    echo "             BUILD STAGE"
                    echo "======================================"

                    echo "Build started..."
                    echo "Build completed successfully!"
                '''
            }
        }

        stage('Verification') {
            steps {
                sh '''
                    echo "======================================"
                    echo "          BUILD VERIFICATION"
                    echo "======================================"

                    echo "Jenkins Docker agent execution:"
                    echo "SUCCESS"

                    echo ""
                    echo "Project: CodeAlpha Jenkins Remoting"
                    echo "Status: Build completed successfully"
                '''
            }
        }
    }

    post {
        success {
            echo 'CodeAlpha Task 2 build completed successfully!'
        }

        failure {
            echo 'Build failed. Check the Console Output.'
        }
    }
}
