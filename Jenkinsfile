#!/usr/bin/env groovy

// node('master') {
//     stage('say-hello') {
//         sh "echo 'hello world !!!'"
//     }
// }

properties([pipelineTriggers([githubPush()])])

node {
    git url: 'https://github.com/someone/something.git', branch: 'master'
}
