#!groovy

node('local') {

    stage('checkout') {
        checkout scm
    }

    stage('do something....') {
        dir('folder') {
            sh './script.sh unknown place'
        }
    }
    stage('....again but with params') {
        dir('folder') {
            withEnv(['param1=abcd']) {
                sh './script.sh ${env.param1} place'
            }
        }
    }
    stage('Done') {
        sh 'echo Done test2'
    }
}
