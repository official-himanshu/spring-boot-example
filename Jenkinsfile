pipeline
{
    agent any
    stages
    {
        stage('deploy')
       {
        echo 'branch name ' + env.BRANCH_NAME
         if(env.BRANCH_NAME.startsWith("testing")
             {
                 steps
                    {
                    sh 'echo "Working in development branch"'
                     sh "mvn clean compile"
                     sh "mvn test"
                     }


             }
         else if(env.BRANCH_NAME.startsWith("testing")
             {
                 steps
                     {
                     sh 'echo "Working in testing branch"'
                     sh "mvn clean compile"
                     sh "mvn test"

                     }
             }
        else if(env.BRANCH_NAME.startsWith("Production")
        {
          steps
          {
            sh 'echo "Working in Production branch"'
            sh "mvn clean compile"
            sh "mvn test"
            sh "mvn package"
            sg degg



          }
        }
          else if(env.BRANCH_NAME.startsWith("testing")
          {
            steps
            {
            sh 'echo "Working in testing branch"'
            sh "mvn clean compile"
            sh "mvn test"

            }
            }





        }




    }



}