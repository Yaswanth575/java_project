node{
    
    def buildNumber = BUILD_NUMBER
    
    stage("Maven Clean Package"){
        def mavenHome= tool name: "Maven", type: "maven"
        sh "${mavenHome}/bin/mvn clean package"
        
    }
    stage('Upload War To Nexus'){
        steps{
            nexusArtifactUploader credentialsId: '301a3d41-a5a4-478b-b962-971f178fb731', groupId: 'group', nexusUrl: '13.40.34.215:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'devops-project', version: '1'
        }
    }
    
}
