pipeline {
  agent any
  stages {
    stage('Prepare')   {
         steps{
                sh 'npm install'
                java -jar /path/to/mta.jar --mtar out.mtar --build-target XSA build
		}
    }
   stage('Build')   {
        steps{
                sh 'karma start karma-ci.conf.js'

        }
    }
    stage('Deploy')   {
        steps{
          sh 'grunt --username='+env.username+' --password="'+env.password+'" --server="http://in-blr-1709:8000" --request="S48K901194" --pkg="ZDEVOPS"' 
        }
    }
  }
}