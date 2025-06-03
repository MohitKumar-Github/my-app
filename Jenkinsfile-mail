node{
  stage('SCM Checkout'){
    git 'https://github.com/MohitKumar-Github/my-app'
    echo 'Successfully checkout'
  }
  stage('Compile Package'){
    //Get Maven Home path
    def mvnHome = tool name: 'maven 3.9', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Email Notification'){
    mail bcc: '', body: '''Hi Welcome to jenkins mail alerts 
thanks 
mohit''', cc: '', from: '', replyTo: '', subject: 'Jenkins job', to: 'mohitkumar9758@gmail.com'
  }
}
