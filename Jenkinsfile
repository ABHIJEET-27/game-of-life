node {
    stage('SCM') {
        git 'https://github.com/ABHIJEET-27/game-of-life.git'
    }
    
    stage('build & package') {
        sh 'mvn package'
    }
    
    stage('output archive artefact') {
        archiveArtifacts 'gameoflife-web/target/gameoflife.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
        
    }
}