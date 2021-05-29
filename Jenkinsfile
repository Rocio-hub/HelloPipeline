pipeline {
    agent any
    triggers {
        pollSCM("* * * * *")
    }
    stages {
        stage("MyFirstStage") {
            steps {
                echo "We are running"
            }
        }
        stage("Test stage: goal: blue ball") {
            steps {
                echo "test"
            }
        }
    }
}