node {
    stage('Download') {
    git branch: 'dev', url: 'https://github.com/clouddevopseng/9am-new-project.git'
     }
    stage('Artifacts convert') {
    sh 'mvn package'
     }
    stage('Deploy into tomcat container') {
    deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'f1c9c42d-414e-45f2-8a4e-141cded58af0', path: '', url: 'http://172.31.8.185:8080')], contextPath: '/new-dev-app', war: '**/*.war'
     }  
}
