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
                sh "bundle install"
                sh "bundle update --bundler"
            }
        }
        stage("Test") {
            steps {
                sh "echo 'teste'"
            }
        }
    }
}