echo 'Hello Marie'

 withCredentials([[$class: 'StringBinding', credentialsId: 'ors_slack_token', variable: 'mytoken']]) 
    {
        //Sending slack Notification
        slackSend(message: 'test slack Notifier plugin from' + env.JOB_NAME+ '-' + env.BUILD_NUMBER, teamDomain: 'autodesk', token: env.mytoken, channel: '#tech-markdown-github', color: 'good')
    }

notifyEmail("PASS","marie.salet@autodesk.com")


//@NonCPS
def notifyEmail(result, to)
{
  def subject = "PASS: MDTet"
  def body = "Hi there, this is a notification that Jenkins has successfully run our stuff."
  // code below sends email using subject and body defined above
  emailext body: body, 
           subject: subject, 
           cc: 'marie.salet@autodesk.com',
           replyTo: 'noreply@autodesk.com', // change this to the reply-handling address
           to: to, // change this to the address to which you wish to send notifications
           attachLog: true, 
           mimeType: 'text/html'
}
