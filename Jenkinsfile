pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
                stage('Email Notification'){
                    mail bcc: '', body: 'Hi  user ,please be ensure the setting and configuration in Jenkins', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'ashwath1219@gmail.com'
            }
        }
    }
}
    }
