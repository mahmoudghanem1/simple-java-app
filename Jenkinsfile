pipeline{
    agent{
        label 'aws-agent'
    }
      stages{
    stage('build'){
      steps{
        script{
          sh  'mvn clean package'
        }
      }
    }
  }
post {
  failure {
slackSend channel: '#devops', message: '"Build Started: ${env.JOB_NAME} ${env.BUILD_NUMBER}"', teamDomain: 'mahmoud-ghanem', tokenCredentialId: 'slack-notif'  }
}
post {
  success {
slackSend channel: '#devops', message: '"Build Started: ${env.JOB_NAME} ${env.BUILD_NUMBER}"', teamDomain: 'mahmoud-ghanem', tokenCredentialId: 'slack-notif'  }
}



}

