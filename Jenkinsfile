pipeline {

   agent any

   stages{

      stage("build")
     {
       steps{
         echo 'Building the application'
       }
     }

       stage("test")
     {
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
