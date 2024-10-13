pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    docker.build('my-application')
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    docker.image('my-application').run('-p 3000:3000')
                }
            }
        }
    }
}

