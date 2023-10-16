pipeline{
    agent {
      label 'aws-agent'
    }
    
    

    stages{
        stage('build'){
            steps{
                script{
                    sh "mvn clean packages"
                }
            }
        }
        stage('test'){
            steps{
                script{
                    echo "test in progress "
                }
            }
        }
    }
}
