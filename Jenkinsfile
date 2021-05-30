pipeline {
    agent any
    triggers {
        pollSCM("* * * * *")
    }
    stages {
        stage("Git merge") {
            steps {
                sh "git fetch --all" //To fetch all branches within the repository: to get all the commits within all the branches so I will get all the commit information.
                sh "git checkout master" //To check out the master branch.
                sh "git pull" //To pull out the master branch to make sure I have everything.
                sh "git merge origin/master" //To make sure that the code base within the master branch and the code base within the feature branch can actually work together.
            } //If I get a merge conflict, the stage will fail and never continue to the Build, Test and Deliver stages.
        }
        stage("Build") {
            steps{
                echo "Build stage"
            }
        }
        stage("Test") {
            steps{
                echo "Test stage"
            }
        }
        stage("Deliver") {
             steps{
                echo "Deliver stage"
            }
        }
    }
}
