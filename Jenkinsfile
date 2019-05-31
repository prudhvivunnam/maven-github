pipeline {
    agent none

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn test'
                }
            }
        }


        stage ('install Stage') {
            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn install'
                }
            }
        }
    }
}
