pipeline{
    stages{
        stage('SCM Checkout'){
            steps{
                git 'https://github.com/jenkinsmohan/7am-web-2019-oct'
                echo "mohansample"
            }
        }
        stage('Maven Build'){
            steps{
                sh 'mvn clean package'
            }
        }
    }
}