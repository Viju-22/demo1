pipeline
{
    agent any
    stages{
        stage('Build Application'){
        steps{
        bat 'mvn clean package'
        }
      
        }
        
        
       
        stage('Publish to Nexus'){
        steps{
		
		nexusArtifactUploader artifacts: [[artifactId: 'scattergather', classifier: '', file: 'target/scattergather-1.0.0-mule-application.jar', type: 'jar']], credentialsId: 'nexusCred', groupId: 'd00fa00a-dbd0-4f71-9676-1f95d2eba6e3', nexusUrl: 'localhost:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'nexusDemo1', version: '1.0.0'
        }
        }
       
   
    }
}
