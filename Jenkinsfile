node{
    
    def buildNumber = BUILD_NUMBER
    
    stage("Git Clone"){
        git url: 'https://github.com/Yaswanth575/java_project.git', branch: 'master'
    }
    
    stage("Maven Clean Package"){
        def mavenHome= tool name: "Maven", type: "maven"
        sh "${mavenHome}/bin/mvn clean package"
        
    }
    
}
