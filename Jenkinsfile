pipeline{
    triggers{
        pollSCM('H 0 * * 2')
     }
  agent any
  
  tools {
  maven 'maven'
  jdk 'java'
}
    
    stages{
        stage("Clean"){
            steps{
                sh 'mvn clean'
            }
        }
      stage("Test"){
          steps{
                sh 'mvn clean test'
            }
        }

    }
    post{
        // always{
        //     //echo "========always========"
        // }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}

