pipeline {
   agent any

   parameters {
      string(name: 'userName', description: 'Name of user to say hello', defaultValue: 'jpascual')
   }

   stages {
      stage('Hello') {
         steps {
            sh """
               echo Hello ${params.userName}!
               """
         }
      }
   }
}
