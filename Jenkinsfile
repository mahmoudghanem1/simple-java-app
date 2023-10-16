pipeline{
    agent any
    

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
