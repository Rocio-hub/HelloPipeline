pipeline {
    agent any
    triggers {
        pollSCM("*****")
    }
    stages {
        stage("MyFirstStage") {
            steps {
                echo "We are running"
            }
        }
    }
}