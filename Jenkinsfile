pipeline {
  agent any
  stages {
    stage('Prepare')   {
         steps{                               
		// java -jar mta.jar --mtar out.mtar --build-target XSA build
		 java -jar mta.jar --build-target XSA build
		}
    }
  }
}
