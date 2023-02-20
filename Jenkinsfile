pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }

    stages{
        stage("Build"){
            steps{
                script {
                    for (int i = 0; i<10; i++) {
                        echo("Script ${i}")
                    }
                }
                echo("Start Build")
                sh("./mvnw clean compile test-compile")
                echo("Finish Build")
            }
        }
        stage("Test"){
            steps{
                echo("Start Test")
                sh("./mvnw test")
                echo("Finish Test")
                // echo "Hello Test 1"
                // sleep(5)
                // echo "Hello Test 2"
                // echo "Hello Test 3"
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