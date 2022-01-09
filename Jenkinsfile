pipeline {
    agent any
    stages {
        stage('Build mvn packege') {
            steps {
                git branch: 'master',
                credentialsId: '8ball92',
                url: 'https://github.com/8ball92/maven-hello-world.git'
                sh "cd my-app ; ls -la && mvn compile"
                    
                
        
                
            }
        }
        stage('Building image') {
            steps {
                sh "pwd && ls -la"
                cleanWs deleteDirs: true, patterns: [[pattern: '', type: 'EXCLUDE']]    
                
            }
        }
    }
}
