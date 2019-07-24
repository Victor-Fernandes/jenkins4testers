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
                
                //sh "chmod +x build/alpine.sh"
                //sh "./build/alpine.sh"
                sh "bundle update --bundler"
                sh "bundle install"
            }
        }
        stage("Test") {
            steps {
                sh "echo 'teste'"
            }
        }
    }
}