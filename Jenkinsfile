pipeline {
    agent any
    stages {
        stage('Build mvn packege') {
            steps {
                git branch: "${env.BRANCH}",
                url: 'https://github.com/8ball92/maven-hello-world.git'
                sh "cd my-app && mvn package " 
                  
            }
        }
        stage('Building image') {
            steps {
                sh "docker build -t ${env.APP}:${env.TAG_VERSION} ."
                
            
                    
                
            }
        }

    }
    post {
        always {
            script {
                echo "THE END JOB"
                sh "docker rmi ${env.APP}:${env.TAG_VERSION}"
                
            }
            
            cleanWs deleteDirs: true, patterns: [[pattern: '', type: 'EXCLUDE']]
        }
    }        
}
