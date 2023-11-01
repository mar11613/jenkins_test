
pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        script{
        def workspace = WORKSPACE
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
          sh "mv  $WORKSPACE/workspacetest.txt  $WORKSPACE/newworkspace.txt" 
          
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
