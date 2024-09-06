pipeline {

   agent any
   parameters{
      choice(name: 'VERSION',  choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
      booleanParam(name: 'executeTests', defaultValue: true, description: '')

   }
   stages{

      stage("build")
     {
        when {
           
       steps{
         echo 'Building the application'
         echo "This is version ${NEW_VERSION}"
       }
     }

       stage("test")
     {
       when {
             expression {
                params.executeTests
             }
       }
       steps{
         echo 'Testing the application'
       }
     }

       stage("deploy")
     {
       steps{
         echo 'Deploying the application'
       }
     }
   }

post {
   always{
       echo 'In always loop'
   }
   success
   {
      echo 'In success loop'
   }

   failure
   {
      echo 'In success loop'
   }
}
}
