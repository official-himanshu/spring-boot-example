pipeline{
    agent{
        label "slave"
    }
    tools { 
        maven 'maven' 
        jdk 'jdk 11'
    }
    stages{
	    
        stage("building"){
            steps{
                sh "mvn compile"
		 
            }
        }
	 stage('Testing') {
            steps {
                echo 'Testing the application...'
                sh "mvn clean test"
            }
        }


    }
    post{
        always{
            mail to: 'mayuri.dhote@knoldus.com',
			subject: "Pipeline: ${currentBuild.fullDisplayName} is ${currentBuild.currentResult}",
			body: "${currentBuild.currentResult}: Job ${env.JOB_NAME} build ${env.BUILD_NUMBER}\n More info at: ${env.BUILD_URL}"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
       
        
