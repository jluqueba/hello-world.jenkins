pipeline {
   agent any
   environment {
      GENERIC_WEBHOOK_TOKEN = credentials('helloWorldMultiBrachToken')
   }
   triggers
   {      
      GenericTrigger(
         genericVariables: [
            [key: 'userName', value: '$.userName', defaultValue: 'jluqueba']
         ],
         token: env.GENERIC_WEBHOOK_TOKEN,
         printContributedVariables: true,
         printPostContent: true,
         silentResponse: false
      )
   }
   stages {
      stage('Hello') {
         steps {
            sh """
               echo Hello $userName!
               """
         }
      }
   }
}