#!/usr/bin/env groovy

// node('master') {
//     stage('say-hello') {
//         sh "echo 'hello world !!!'"
//     }
// }

properties([pipelineTriggers([githubPush()])])

node {
    stage('Github') {
        git url: 'https://github.com/raphaelcoutu/workflow.git', branch: 'master'    
    }
    stage('Output') {
        sh "echo 'hello world'"
        sh "echo 'NICE...'"
    }
}
