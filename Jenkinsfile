pipeline {
    agent any
    stages {
        stage('Start') {
            steps {
                echo 'Start'
            }
        }
        stage('None') {
            when {
                branch '*/none'
            }
            steps {
                echo 'NONE World'
            }
        }
        stage('Master') {
            when {
                branch '*/master'
            }
            steps {
                echo 'Master Branch'
            }
        }
        stage('Example') {
            steps {
                parallel (
                    "english" : {
                        echo 'Hello World'
                    },
                    "francais" : {
                        echo 'Bonjour le monde'
                    }
                )
            }
        }
        stage('End') {
            steps {
                echo 'The END'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
