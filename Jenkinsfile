pipeline {
agent any

stages {
    stage('Build') {
        steps {
            sh 'wget https://raw.githubusercontent.com/composer/getcomposer.org/1b137f8bf6db3e79a38a5bc45324414a6b1f9df2/web/installer -O - -q | php -- --quiet'
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
