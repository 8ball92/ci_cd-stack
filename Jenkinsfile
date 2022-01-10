pipeline {
    agent any
    environment {
        ENV_NAME = "${env.BRANCH}"
    }
    stages {
        stage('Build mvn packege') {
            steps {
                git branch: "${env.BRANCH}",
                // credentialsId: '8ball92',
                url: 'https://github.com/8ball92/maven-hello-world.git'
                sh "cd my-app ; mvn package " 
                // sh "java -cp my-app/target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App"  
            }
        }
        stage('Building image') {
            steps {
                print(env.BRANCH)
            
                cleanWs deleteDirs: true, patterns: [[pattern: '', type: 'EXCLUDE']]    
                
            }
        }

    }
    post {
        always {
            script {
                echo "the end"
             }
        }
    }        
}
