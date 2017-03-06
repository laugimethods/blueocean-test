pipeline {
    agent any
    stages {
        stage('Start') {
            steps {
                echo 'Start'
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
