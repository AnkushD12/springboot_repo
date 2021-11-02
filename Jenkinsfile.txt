pipeline {
    agent any

    stages {
        stage ('Build Stage') {

            steps {
              
                    bat 'mvn clean'
                    bat 'mvn compile'
                    bat 'mvn package'
                
            }
        }



        stage ('Deployment Stage') {
            steps {
               echo "Deploying Project";
            }
        }
    }
}
