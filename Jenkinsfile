pipeline {
    agent any

    stages {
    stage('git version') {
        steps {
            sh 'git version'
        }
    }
    
    
   
    stage('kubernetes version') {
        steps {
            withKubeConfig([credentialsId: 'config']) {
            sh 'kubectl version --short'
        }
        }
    }
}
}
