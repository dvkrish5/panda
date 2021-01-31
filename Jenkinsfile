pipeline {  
     agent any  
     stages {  
         stage('Test') { 
                   slackSend baseUrl: 'https://hooks.slack.com/services/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/', botUser: true, channel: 'Jenkins-pipeline', color: 'green', message: 'welcome to happy home', notifyCommitters: true
         }  
             steps {  
                 sh 'echo "Fail!"; exit 1'  
             }  
         }  
     }  
     post {  
         always {  
             echo 'This will always run'  
         }  
         success {  
             echo 'This will run only if successful'  
         }  
         failure {  
             mail bcc: 'dvkrish5@gmail.com', body: "<b>Example</b><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}", cc: '', charset: 'UTF-8', from: '', mimeType: 'text/html', replyTo: '', subject: "ERROR CI: Project name -> ${env.JOB_NAME}", to: "foo@foomail.com";  
         }  
         unstable {  
             echo 'This will run only if the run was marked as unstable'  
         }  
         changed {  
             echo 'This will run only if the state of the Pipeline has changed'  
             echo 'For example, if the Pipeline was previously failing but is now successful'  
         }        
     }  
 }
}
