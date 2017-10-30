pipeline {
    
     agent any
    
    stages {
        stage ('Compilation first build Stage') {

            steps {
                
                    sh 'mvn clean compile'
                
            }
        }

        stage ('Testing Junit cases Stage') {

            steps {
                
                    sh 'mvn test'
                
            }
        }


        stage ('Deployment Final Stage') {
            steps {
                 
                    sh 'mvn deploy'
                
            }
        }
    }
}
