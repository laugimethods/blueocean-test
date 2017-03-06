pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                parallel (
                    echo 'Hello World'
                    echo 'Bonjour le monde'
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
