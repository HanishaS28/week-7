pipeline {
    agent any
    environment {
        PATH = "C:\\Program Files\\Docker\\Docker\\resources\\bin;${env.PATH}"
        DOCKER_HOST = 'tcp://localhost:2375'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building Docker Image..."
<<<<<<< HEAD
                bat "docker build -t mypythonflaskapp ."
=======
                bat 'cd "week-7" && docker build -t mypythonflaskapp .'
>>>>>>> 88e71344da47ce2d5cd469dd4ce0088b8799fa5e
            }
        }
        stage('Run') {
            steps {
                echo "Running Docker Container..."
<<<<<<< HEAD
                bat "docker rm -f mycontainer || exit 0"
                bat "docker run -d -p 5000:5000 --name mycontainer mypythonflaskapp"
=======
                bat 'docker rm -f mycontainer || exit 0'
                bat 'docker run -d -p 5000:5000 --name mycontainer mypythonflaskapp'
>>>>>>> 88e71344da47ce2d5cd469dd4ce0088b8799fa5e
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
