pipeline {

    agent any
 
    tools {

        // Install the Maven version configured as "M3" and add it to the path.

        maven "M3"

    }
 
    stages {

        stage('Build') {

            steps {


                // Run Maven on a Unix agent.

                sh "mvn -Dmaven.test.failure.ignore=true clean package"
 
                // To run Maven on a Windows agent, use

                // bat "mvn clean compile"

            }

        }

        stage('Test'){

            steps {

                sh "mvn test"

            }
        }

        stage('Package'){
            steps{
                sh "mvn -Dmaven.test.skip test"
            }

        }   
    }
}

 