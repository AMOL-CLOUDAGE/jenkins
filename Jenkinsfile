pipeline {
    agent any

    stages {
    stage('git version') {
        steps {
            sh 'git version'
        }
    }
    
    stage('maven version') {
        steps {
            sh 'mvn -v'
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
