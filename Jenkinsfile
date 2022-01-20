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
        stage('tomcat dev'){
            steps{
                sshagent(['tomcat-dev']) {
                // stop tomcat
                sh "ssh -o StrictHostKeyChecking=no ec2-user@44.202.133.126 /opt/tomcat9/bin/shutdown.sh"
                //copy war file
                sh "scp target/*.war ec2-user@44.202.133.126 /opt/tomcat9/webapps/devops"
                //start tomcat
                sh "ssh -o StrictHostKeyChecking=no ec2-user@44.202.133.126 /opt/tomcat9/bin/shutdownstartup.sh"
            }
            }
        }
    }
}


