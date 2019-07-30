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
                sh "./build/alpine.sh"
                sh "gem install bundler:2.0.1" //não fuciona sem instalar o bundler
                sh "bundle install"
            }
        }
        stage("Test") {
            steps {
                sh "bundle exec cucumber -p ci"
                cucumber failedFeaturesNumber: -1, failedScenariosNumber: -1, failedStepsNumber: -1, fileIncludePattern: '**/*.json', jsonReportDirectory: 'log', pendingStepsNumber: -1, skippedStepsNumber: -1, sortingMethod: 'ALPHABETICAL', undefinedStepsNumber: -1
            }
        }
    }
}