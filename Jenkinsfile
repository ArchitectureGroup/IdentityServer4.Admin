pipeline {
    agent any
    stages {

        stage('Start deployment') {
            steps {
                echo 'Start deployment'
                sh 'printenv'
            }
        }

        stage('build-image') {
            steps {
                retry(2) { sh "docker version"}
                retry(2) { sh "docker-compose --version"}
            }
        }

        stage('deploy') {
            steps {
                echo 'Deployment complete'
            }
        }
    }
}

