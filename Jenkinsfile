pipeline {
    agent any
    // environment {
    //     ENV_NAME = "${env.BRANCH}"
    //     ENV_TAG = "${env.TAG_VERSION}"
    // }
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
                sh "docker build -t ${env.APP}:${env.TAG_VERSION} ."
                // sh "ls -la && pwd"
                print(env.BRANCH)
                print(env.TAG_VERSION)
            
                    
                
            }
        }

    }
    post {
        always {
            script {
                echo "THE END JOB"
            }
            cleanWs deleteDirs: true, patterns: [[pattern: '', type: 'EXCLUDE']]
        }
    }        
}
