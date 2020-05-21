pipeline {
  agent any
  stages {
    stage('Prepare')   {
         steps{
                sh 'npm install'
                java -jar /com.sap.cloud.lm.sl.mta-1.81.0.jar --mtar out.mtar --build-target XSA build
		}
    }
   stage('Build')   {
        steps{
                echo "Build"

        }
    }
    stage('Deploy')   {
        steps{
          echo "Deploy"
        }
    }
  }
}
