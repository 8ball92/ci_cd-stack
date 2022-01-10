pipeline {
    agent any
    environment {
        ENV_NAME = "${env.TESTE}"
    }
    stages {
        stage('Build mvn packege') {
            steps {
                git branch: 'master',
                credentialsId: '8ball92',
                url: 'https://github.com/8ball92/java-hello-world-maven.git'
                sh "mvn mvn package"
                sh "ls -la src/main/java"   
            }
        }
        stage('Building image') {
            steps {
                print(env.TESTE)
            
                cleanWs deleteDirs: true, patterns: [[pattern: '', type: 'EXCLUDE']]    
                
            }
        }
    }
}
