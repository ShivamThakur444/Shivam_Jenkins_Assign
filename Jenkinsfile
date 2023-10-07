pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               //bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                bat "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                bat "mvn install TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                bat "mvn test TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                bat "mvn package TicketBookingServiceJunitTesting"
            }
        }
    }
}
