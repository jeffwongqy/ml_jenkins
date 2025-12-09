pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                script {
                    // Install necessary Python packages
                     bat "pip install -r requirements.txt"
                }
            }
        }

        stage('Load and Preprocess Data') {
            steps {
                script {
                    // Run data loading script
                    bat "python data_loading.py"
                }
            }
        }

        stage('Train Model') {
            steps {
                script {
                    // Run model training script
                    bat "python model_training.py"
                }
            }
        }

        stage('Evaluate Model') {
            steps {
                script {
                    // Run model evaluation script
                    bat "python model_evaluation.py"
                }
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '**.pkl', fingerprint: true
            echo 'Pipeline execution complete.'
        }
    }
}
