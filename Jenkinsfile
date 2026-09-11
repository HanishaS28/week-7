pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building Docker Image..."
                bat "docker build -t mypythonflaskapp ."
            }
        }

        stage('Run') {
            steps {
                echo "Deploying application in Docker Container..."
                // Forcibly stop and remove any existing container named 'mycontainer'
                bat "docker rm -f mycontainer || exit 0"
                
                // Run the container in detached mode on port 5000
                bat "docker run -d -p 5000:5000 --name mycontainer mypythonflaskapp"
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
