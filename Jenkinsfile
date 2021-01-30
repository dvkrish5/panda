post {
always {
  script {
    if (currentBuild.currentResult == 'FAILURE') {
      step([$class: 'Mailer', notifyEveryUnstableBuild: true, recipients: "ashwath1219@gmail.com", sendToIndividuals: true])
    }
  }
