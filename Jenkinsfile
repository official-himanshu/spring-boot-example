pipeline{
    agent any
    tools { 
        maven 'maven3'
    }
    stages
       {
            stage("clean")
            {
                steps{
                    sh "mvn clean"
                }
            }
            stage("Build")
            {
                steps{
                    sh "mvn compile"
                }
                
            }
            stage("package")
            {
                steps{
                    sh "mvn package"
                }
            }


        }
    
}
