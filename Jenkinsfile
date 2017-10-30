pipeline {
    
     agent any
    
    stages {
        stage ('Compilation build Stage') {

            steps {
                
                    sh 'mvn clean compile'
                
            }
        }
        stage ('Valdiate Stage') {

            steps {
                
                    sh 'mvn validate'
                
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
