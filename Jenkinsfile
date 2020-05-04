pipeline {
   agent any
   environment {
      TOKEN = credentials('helloWorldMultiBrachToken')
   }
   triggers
   {      
      GenericTrigger(
         genericVariables: [
            [key: 'userName', value: '$.userName']
         ],
         token: env.TOKEN,
         printContributedVariables: true,
         printPostContent: true,
         silentResponse: false
      )
   }
   stages {
      stage('Hello') {
         steps {
            sh "echo Hello $userName"
         }
      }
   }
}