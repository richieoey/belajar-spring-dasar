pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }

    stages{
        stage("Hello"){
            steps{
                echo "Hello World"
            }
        }
        stage("test"){
            steps{
                echo "Test"
            }
        }
    }

    post {
        always {
            echo "I will always say Hello World"
        }
        success {
            echo "Success !"
        }
        failure {
            echo "Oh no, Failed"
        }
        cleanup {
            echo "Don't care success or error"
        }
    }
}