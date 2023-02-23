pipeline {
    agent none


    stages{
        stage("Build"){
            agent {
                node {
                    label "linux && java11"
                }
            }
            steps{
                script {
                    // Script Tutorial
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
            agent {
                node {
                    label "linux && java11"
                }
            }
            steps{
                script{
                    def data = [
                        "firstName" : "Richie",
                        "lastName" : "Oey"
                    ]
                    writeJSON(file: "data.json", json: data)
                }
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
            agent {
                node {
                    label "linux && java11"
                }
            }
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