pipeline{
    parameters {
        run description: 'Choose name', filter: 'ALL', name: 'name', projectName: 'Hari'
        choice choices: ['Bangalore', 'Pune', 'Delhi', 'Noida'], description: 'Choose your location', name: 'location'
    }
    agent any
    stages{
        stage('Hello'){
            echo "Your name is {params.name}"
            echo "your location is {params.location}"
        }
    }
}


