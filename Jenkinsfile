pipeline {
    agent { 
      docker { image 'docker pull python:3.8.16-bullseye' }
    }
    stages {
       stage ("Run the script") {
            steps {
                withAWS(credentials: 'awscredID', region: 'us-east-1'){
                    sh "pip3 install -r requirements.txt"
                    sh "python3 check_endpoint.py"
                }
            }
        }
    }
}
