properties([
        disableConcurrentBuilds(),
])

node {
    stage('checkout') {
        checkout scm
    }

    try {
        stage('build') {
            sh "echo build"
            slackSend color: 'good', message: "jenkins notification test"
        }
    } catch(err) {
        sh "echo error"
        slackSend color: 'danger', message: "jenkins error"
    } finally {
        stage('cleanup') {
            sh "echo cleanup"
        }
    }
}
