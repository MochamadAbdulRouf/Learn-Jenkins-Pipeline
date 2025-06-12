pipeline {
    agent {
        node {
            label "linux && java17"
        }
    }
    stages {
        stage ("Hello") {
            steps {
                echo ("Hello Pipeline")
            }
        }
    }

    post {
        always {
            echo "i will always say hello!!"
        }
        success {
            echo "i will say success only when the build is successful!!"
        }
        failure {
            echo "i will say failed only when the build is failed!!"
        }
        cleanup {
            echo "i will say clean only when the build is cleaned up!!"
        }
    }
}