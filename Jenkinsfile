pipeline {
    agent any
     tools { 
        maven 'maven-3.5.2'  
    }
    stages {
        stage ('Compile Stage') {

            steps {
		    sh 'rm -rf mavennexusjenkinsfirst'
		    sh 'git clone https://github.com/arjunksofficial/mavennexusjenkinsfirst.git'
		    sh 'cd mavennexusjenkinsfirst'

            }
        }

        stage ('Testing Stage') {

            steps {
            
            sh 'mvn --settings settings.xml install -Dmaven.test.skip=true'
            sh 'mvn --settings settings.xml package -Dmaven.test.skip=true'
            
            }
        }


        stage ('Deployment Stage') {
            steps {

                    sh 'mvn --settings settings.xml deploy -Dmaven.test.skip=true'

            }
        }
    }
}
