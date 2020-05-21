pipeline {
   agent any
   triggers
   {      
      GenericTrigger(
         genericVariables: [
            [key: 'userName', value: '$.userName', regexpFilter: '[^0-9]']
         ],
         // token: '5cb90505dc1b874d5d2731553f5f8f1b3499e33e',
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