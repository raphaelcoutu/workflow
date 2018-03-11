#!/usr/bin/env groovy

// node('master') {
//     stage('say-hello') {
//         sh "echo 'hello world !!!'"
//     }
// }

properties([pipelineTriggers([githubPush()])])

node {
    git url: 'https://github.com/raphaelcoutu/workflow.git', branch: 'master'
}
