pipeline {
    agent {
        //agent docker ruby para executar os testes
        docker {
            image "ruby:alpine"
        }
    }
    stages {
        stage("Build") {
            steps {
                sh "chmod +x build/alpine.sh"
                sh "./buid/alpine.sh"
                sh "bundle install"
            }
        }
        stage("Test") {
            steps {
                sh "bundle exec cucumber -p dev"
            }
        }
    }
}