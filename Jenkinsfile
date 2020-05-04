pipeline {
   agent any
   triggers {
      GenericTrigger(
         genericVariables: [
            [key: 'userName', value: '$.userName']
         ],
         token: 'abc123',
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