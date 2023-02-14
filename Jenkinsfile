pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS667 hello-world.cpp'
                build job: 'PES1UG20CS667-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS667'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Build Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
