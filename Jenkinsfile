pipeline {
    agent any
    stages {
        stage('Build mvn packege') {
            steps {
                git branch: "${env.BRANCH}",
                credentialsId: 'github',
                url: 'https://github.com/8ball92/maven-hello-world.git'
                
                // sh "mvn package " 
                // sh "java -cp my-app/target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App"  
            }
        }
        // stage('Building image') {
        //     steps {
        //         sh "docker build -t ${env.APP}:${env.TAG_VERSION} ."
                
            
                    
                
        //     }
        // }

    }
    // post {
    //     always {
    //         script {
    //             echo "THE END JOB"
    //             sh "docker rmi ${env.APP}:${env.TAG_VERSION}"
                
    //         }
            
    //         cleanWs deleteDirs: true, patterns: [[pattern: '', type: 'EXCLUDE']]
    //     }
    // }        
}
