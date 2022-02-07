pipeline{
    agent{
        label 'Master'
    }
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
             stage("TEST")
            {
                steps{
                    sh "mvn test"
                }
            } 


        }
         post {
        always{
            mail to: 'shivam.pateriya@knoldus.com',
		    subject: "Pipeline info",
			body: "your build is ${currentBuild.currentResult}: Job ${env.JOB_NAME} build ${env.BUILD_NUMBER}"
        }
         success {
            echo "Application is build succesfully"
        }
        failure {
            echo "Application is failed"
        }
    }
    
}
