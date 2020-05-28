pipeline {
  agent any
  stages {
stage('Git Checkout') {
        steps{
            checkout poll: true,
            scm: [$class: 'GitSCM', branches: [[name: 'master']],
            userRemoteConfigs: [[credentialsId: "", url: 'https://github.com/rajendrasharma1000/SAP_CAP.git']]]
        }
    }
    stage('Prepare')   {
         steps{                               
		// java -jar mta.jar --mtar out.mtar --build-target XSA build
		 java -jar /mta.jar --build-target XSA build
		}
    }
  }
}
