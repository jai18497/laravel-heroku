pipeline {
agent any

stages {
    stage('Build') {
        steps {
            sh 'composer install --no-interaction'
            sh 'npm run prod'
            sh 'run some other commands to compile assets'
        }
    }
    stage('Test') {
        steps {

            sh './vendor/bin/phpunit'

        }
    }
}
}
