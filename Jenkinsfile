pipeline {
    agent any
        stages {
        stage ('check'){
            steps{
                git 'https://github.com/Keltzu/cal_3013_demo.git'
            }
        }
        stage ('build'){
            steps{
                bat 'mvn clean install'
            }
        }

        stage('test') {
            steps{
                bat 'mvn test'
            }
        }
        stage('jacoco'){
            steps{
                jacoco()
            }
        }

    }
}