pipeline {
   agent any
   triggers
   {
      withCredentials([string(credentialsId: 'helloWorldMultiBrachToken', variable: 'token')]) {         
         GenericTrigger(
            genericVariables: [
               [key: 'userName', value: '$.userName']
            ],
            token: token,
            printContributedVariables: true,
            printPostContent: true,
            silentResponse: false
         )
      }
   }
   stages {
      stage('Hello') {
         steps {
            sh "echo Hello $userName"
         }
      }
   }
}