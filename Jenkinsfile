pipeline {
   agent any
   withCredentials([string(credentialsId: 'helloWorldMultiBrachToken', variable: 'token')])
   {
      triggers {         
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