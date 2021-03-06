pipeline {
    agent any
    tools {
    maven 'maven-3.6.3'
  }
    stages {
        
        stage ('Build') {
            steps {
                echo 'This is a minimal pipeline.'
            }
        }
        stage('Notify') {
                withAWS(credentials: 'awsCredentials') {
                    snsPublish(topicArn: 'arn:aws:sns:us-east-1:518523660471:JenkinsNotification', subject: 'DISA-DEMO-DEV Build - success', message: 'Jenkins build is successful')
                }
        }
    }
}
