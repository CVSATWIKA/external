pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Building docker image'
                bat 'docker build -t kubedemoapp:v1 .'
            }
            
        }
        stage('Run'){
            steps{
            echo 'Running docker container'
            bat 'docker run -d -p 5000:5000 myapp:latest'
        }
        }
    
    }
    post{
        success{
            echo 'Build and Run Successful'
        }
        failure{
            echo 'Build and Run Failed'
        }
    }
}