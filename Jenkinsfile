pipeline {
    agent any

    environment {
        // Update this path to your actual python.exe
        PYTHON = "C:\\Program Files\\Python314\\python.exe"
    }

    stages {
        stage('Test Python Environment') {
            steps {
                script {
                    // Check Python version
                    bat "\"${env.PYTHON}\" --version"

                    // Check pip version
                    bat "\"${env.PYTHON}\" -m pip --version"

                    // Run a small Python command to verify execution
                    bat "\"${env.PYTHON}\" -c \"print('Python environment is working!')\""
                }
            }
        }
    }
}
