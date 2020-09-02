pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'Maven 3.6.3' 
    }
    

    stages{
        stage('one'){
            steps{
                echo 'this is the build job'
                sh 'mvn compile'
            }
        }
        stage('two'){
            steps{
                echo 'this is the test job'
                sh 'mnv clean test'
            }
        }
        stage('three'){
            steps{
                echo 'this is the job for packaging'
                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}

