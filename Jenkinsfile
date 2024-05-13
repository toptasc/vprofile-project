pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment {
        SNAP REPO = 'vprofile-snapshot'
        NEXUS USER = 'admin'
        NEXUS PASS = '706637'
        RELEASE_REPO = 'profile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.56.192'    
        NEXUSPORT = ' 8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS _LOGIN = 'nexuslogin'|
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}