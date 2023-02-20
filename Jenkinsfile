pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }

    stages{
        stage("Build"){
            steps{
                echo "Hello Build 1"
                sleep(10)
                echo "Hello Build 2"
                echo "Hello Build 3"
            }
        }
        stage("Test"){
            steps{
                echo "Hello Test 1"
                sleep(5)
                echo "Hello Test 2"
                echo "Hello Test 3"
                //sh("error") contoh error
            }
        }
        stage("Deploy"){
            steps{
                echo "Hello Deploy 1"
                sleep(5)
                echo "Hello Deploy 2"
                echo "Hello Deploy 3"
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