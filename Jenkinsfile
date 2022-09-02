pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
tools{
      maven 'maven' 
    }
   

    stages{
        stage('compile-app'){
            steps{
                echo 'this is the compile job'
                sh 'mvn compile'
            }
        }
        stage('test-app'){
            steps{
                echo 'this is the second job'
                sh 'mvn test'
            }
        }
        stage('package-app'){
            steps{
                echo 'this is the third job'
                sh 'mvn package'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
