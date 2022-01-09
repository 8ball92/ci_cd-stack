pipeline {
    agent any
    stages {
        stage('clone mvn repo') {
            steps {
                git branch: 'master',
                url: 'https://github.com/jabedhasan21/java-hello-world-with-maven.git'

                sh "ls -lat"
                
            }
        }
    }
}
