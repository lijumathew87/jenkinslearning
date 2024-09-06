pipeline {

   agent any
   environment{
      NEW_VERSION = '1.3.0'
   }
   stages{

      stage("build")
     {
       steps{
         echo 'Building the application'
         echo "This is version ${NEW_VERSION}"
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
