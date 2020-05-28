pipeline {
  agent any
  stages {
    stage('Prepare')   {
         steps{
                               
		java -jar mta.jar --mtar out.mtar --build-target XSA build
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
