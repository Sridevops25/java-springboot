pipeline {
  agent any
  
  stages {
    stage('Build'){
      step {
        echo 'Build Phase'
      }
    }
    stage('Test'){
      step {
        echo 'Test Phase'
      }
    }
    stage('Quality Gate- Sonar Cube'){
     step {
        echo 'Sonar Qube'
      } 
    }
    #CD
    stage('Push to Artifactory'){
     step {
        echo 'Push to artifactory'
      } 
    }
    stage('Deploy to QA'){
       step {
        echo 'Deploy to QA'
      } 
    }
    stage('Deploy to Production'){
      step {
        echo 'Deploy to Prod'
      } 
    }
   } 
  post {
    failure{
      echo'Failed'
    }
    success{
      echo'Passed'
    }
    aborted{
    echo'aborted'
    }
    always{
    echo 'always'
    }
   }
  }

