pipeline {
    agent {
        //agent docker ruby para executar os testes
        docker {
            image "ruby"
        }
    }
    stages {
        stage("Build") {
            steps {
                sh "bundle install"
            }
        }
        stage("Test") {
            steps {
                sh "echo 'simulando teste automatizado'"
            }
        }
    }
}