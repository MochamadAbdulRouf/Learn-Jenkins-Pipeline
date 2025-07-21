pipeline {
    agent {
        node {
            label "linux && java17"
        }
    }
    stages {


        stage ("Build") {
            steps {
                echo ("Hello test 1")
                sleep(10)
                echo ("Hello test 2")
                echo ("Hello test 3")
            }
        }

        stage("Test") {
            steps {
                echo("Hello bd 1")
                sleep(5)
                echo ("Hello build 2")
                echo ("Hello build 3")
            }
        }

        stage("Deploy") {
            steps{
                echo("Hello Deploy 1")\
                sleep(5)
                echo("Hello Deploy 2")
                echo("Hello Deploy 3")
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