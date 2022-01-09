// pipeline {
//     agent any
//     stages {
//         stage('build') {
//             steps {
//                 sh 'hostname'
//             }
//         }
//     }
// }
pipeline {
    node('master') {
        stage('GetNodeName') {
        def node_name = "${NODE_NAME}"
        echo "The Node Name is: ${node_name}"
        }
}
    
}