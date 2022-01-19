pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git credentials: 'jenkinsmohan',
                url: 'https://github.com/jenkinsmohan/7am-web-2019-oct',
                branch: 'master'
            }
        }
        stage('Maven Build'){
            steps{
                sh 'mvn clean package'
            }
        }
    }
}