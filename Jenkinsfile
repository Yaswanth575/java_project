
node{
    
    def buildNumber = BUILD_NUMBER
        
    stage("Maven Clean Package"){
        def mavenHome= tool name: "Maven", type: "maven"
        sh "${mavenHome}/bin/mvn clean package"
        
    }
    
}
