pipeline {
agent any

stages {
    stage('Build') {
        steps {
              composer install --no-interaction
        }
    }
    stage('Test') {
        steps {

               ./vendor/bin/phpunit

        }
    }
}
}
