#!/usr/bin/env groovy
properties([pipelineTriggers([githubPush()])])

node {
    stage('build') {
        git url: 'https://github.com/raphaelcoutu/workflow.git', branch: 'master'
        
        sh "./develop up -d"
        sh "./develop composer install"

        sh "cp .env.example .env"
        sh "./develop art key:generate"
        sh 'sed -i "s/REDIS_HOST=.*/REDIS_HOST=redis/" .env'
        sh 'sed -i "s/CACHE_DRIVER=.*/CACHE_DRIVER=redis/" .env'
        sh 'sed -i "s/SESSION_DRIVER=.*/SESSION_DRIVER=redis/" .env'
    }
    stage('test') {
        sh "./develop test"
    }
}
