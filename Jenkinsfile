node {
    stage('Download') {
    git branch: 'test', url: 'https://github.com/clouddevopseng/9am-new-project.git'
     }
    stage('Artifacts convert') {
    sh 'mvn package'
     }
    stage('Deploy into tomcat container') {
    deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: '688da7d5-53af-4485-adb8-76a4c381692d', path: '', url: 'http://13.204.88.141:8080')], contextPath: '/new-test-app', war: '**/*.war
     }  
}
