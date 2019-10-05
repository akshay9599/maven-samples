pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven-3') {
                    sh 'mvn clean package'
                }   
            }
        }

    stages {
        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven-3') {
                    sh 'mvn test'
                }   
            }
        }

    stages {
        stage ('Deployment Stage') {

            steps {
                withMaven(maven : 'maven-3') {
                    sh 'mvn deploy'
                }   
            }
        }

    }
}
