pipeline{
    agent any
    environment {
      PATH = "${PATH}:${tool name: 'maven3', type: 'maven'}/bin"
    }

    stages{
        stage('Maven Build'){
            steps{
                sh 'mvn clean package'
            }
        }
    }
}