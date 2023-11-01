def workspace = WORKSPACE
pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        script{
        
      workspace = env.WORKSPACE
      echo "Current workspace is $WORKSPACE"
          sh "cat  > $WORKSPACE/workspacetest.txt"
          
        }
        }
    }

    stage('Rename'){
      steps{
        script{
          echo "Current workspace is $WORKSPACE"
        }
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }
  }
}
