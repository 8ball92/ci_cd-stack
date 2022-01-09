pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git branch: 'master',
                credentialsId: '8ball92',
                url: 'https://github.com/8ball92/maven-hello-world.git'
                sh "cd my-app"
                sh "mvn compile"
                sh  "ls -la src/target/"    
                cleanWs deleteDirs: true, patterns: [[pattern: '', type: 'EXCLUDE']]
                
                
            }
        }
    }
}
