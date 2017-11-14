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
                    sh 'mvn checkstyle:checkstyle'
            }
        }
        stage('checkStyle Stage'){
            steps {
                step([$class: 'hudson.plugins.checkstyle.CheckStylePublisher', pattern: '**/target/checkstyle-result.xml', healthy:'20', unHealthy:'100'])
            }   
        }
    }
}
