properties([
    buildDiscarder(logRotator(daysToKeepStr: '3', numToKeepStr: '3')),
])
pipeline {

    agent any 
    
    stages {
        
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Code Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: '*/main']], 
                    userRemoteConfigs: [[url: 'https://github.com/revanth-citibank/AxisBank-2023-NewYear.git']]
                ])
            }
        }       

    }   
}
