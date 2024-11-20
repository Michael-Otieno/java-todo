pipeline{
    agent any
    tools {
        gradle 'Gradle-6'
    }
    stages {
        stage("clone repository"){
            steps{
                git branch:"master", url:"https://github.com/Michael-Otieno/java-todo"
            }
        }
        stage("Build code"){
            steps{
                sh 'gradle build'
            }
        }
        stage("Test code"){
            steps{
                sh 'gradle test'
            }
        }
    }
}