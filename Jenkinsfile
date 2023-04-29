pipeline {
    agent any
    stages {
       stage ("Run the script") {
            steps {
                withAWS(credentials: 'aws-credentials', region: 'us-east-1'){
                    sh "pip3 install -r requirements.txt"
                    sh "python3 check_endpoint.py"
                }
            }
        }
    }
}
