pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh '
                    cd project \
                    mvn package
                    '
            }
        }
    }
}
