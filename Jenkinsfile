pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git branch: 'master',
                credentialsId: '8ball92',
                url: 'https://github.com/jabedhasan21/java-hello-world-with-maven.git'
                sh "mvn package"    
                cleanWs deleteDirs: true, patterns: [[pattern: '', type: 'EXCLUDE']]
                
                
            }
        }
    }
}
