pipeline {
  agent any
  
  stages {
    stage('Build'){
      steps{
        echo 'Build Phase'
        sh 'mvn clean package'
      }
    }
    stage('Test'){
      steps{
        echo 'Test Phase'
	      sh 'mvn test'
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
    stage('Deploy to Production'){
      steps{
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

