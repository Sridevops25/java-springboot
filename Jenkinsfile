pipeline {
  agent any
  
  stages {
    stage('Build'){
      steps{
        echo 'Build Phase'
      }
    }
    stage('Test'){
      steps{
        echo 'Test Phase'
      }
    }
    stage('Quality Gate- Sonar Cube'){
     steps{
        echo 'Sonar Qube'
      } 
    }

    stage('Push to Artifactory'){
     steps{
        echo 'Push to artifactory'
      } 
    }
    stage('Deploy to QA'){
       steps{
        echo 'Deploy to QA'
      } 
    }
    stage('Deploy to Staging'){
      steps{
        echo 'Deploy to Staging'
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

