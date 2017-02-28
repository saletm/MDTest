echo 'Hello Marie'

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
           replyTo: 'marie.salet@autodesk.com', // change this to the reply-handling address
           to: to, // change this to the address to which you wish to send notifications
           attachLog: true, 
           mimeType: 'text/html'
}
