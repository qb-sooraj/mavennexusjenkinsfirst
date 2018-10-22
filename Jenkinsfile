pipeline {
    agent any
     tools { 
        maven 'default maven' 
        
    }
    stages {
        stage ('Compile Stage') {

            steps {

                    sh 'mvn --settings settings.xml compile'

            }
        }

        stage ('Testing Stage') {

            steps {

                    sh 'mvn --settings settings.xml package'

            }
        }


        stage ('Deployment Stage') {
            steps {

                    sh 'mvn --settings settings.xml deploy'

            }
        }
    }
}
