pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                    g++ -o YOUR_SRN-1 main.cpp
                    '''
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh '''
                    ./YOUR_SRN-1
                    '''
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment process (Modify as needed)"
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
