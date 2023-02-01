pipeline{
    triggers {
        pollSCM('* * * * *')
    }

    tools {
        maven 'M2_HOME'
    }

    agent any 

    stages{
        stage('maven package'){
            steps{
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('deploy'){
            steps{
                echo 'deployment'
            }
        }
    }
}