pipeline {
    agent any
    stages {
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
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
