pipeline {

    agent any
 
    tools {

        maven 'Maven 3' // Adjust this to your Maven version

    }
 
    stages {

        stage('Checkout Code') {

            steps {

                git 'https://github.com/krsaeed/hello-world.git'

            }

        }
 
        stage('Build with Maven') {

            steps {

                sh 'mvn clean package'

            }

        }
 
        stage('Archive Aritfacts') {

            steps {

                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true

            }

        }

    }

}
 
