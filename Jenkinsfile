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
                sh "gem install bundler:2.0.1"
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