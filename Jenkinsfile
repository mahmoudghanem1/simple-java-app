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
  success {
    slackSend channel: '#devops', message: '"started ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)"', teamDomain: 'mahmoud-ghanem', tokenCredentialId: 'slack-notif'
  }
} 
post {
  always {
        slackSend channel: '#devops', message: '"started ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)"', teamDomain: 'mahmoud-ghanem', tokenCredentialId: 'slack-notif'

  }
}

}
