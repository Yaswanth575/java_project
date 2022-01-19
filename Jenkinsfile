node{
    
    def buildNumber = BUILD_NUMBER
    
    stage("Maven Clean Package"){
        def mavenHome= tool name: "Maven", type: "maven"
        sh "${mavenHome}/bin/mvn clean package"
        
    }
    stage('Upload War To Nexus'){
        steps{
            nexusArtifactUploader artifacts: [[artifactId: 'java-web-app', classifier: '', file: 'target/Maven Web Application-1.0.war', type: 'war']], credentialsId: '', groupId: 'com.mt', nexusUrl: '172.31.4.121:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'devops-project', version: '1.0'
        }
    }
    
}
