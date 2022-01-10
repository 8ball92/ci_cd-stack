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
                url: 'https://github.com/pdurbin/maven-hello-world.git'
                // sh "mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false"
                sh "cd my-app ; mvn package " 
                sh "ls -la"  
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
