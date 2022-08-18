pipeline {
    agent any

    parameters {
    choice(name: 'BranchName', choices:['master','development','stage','qa'], description: 'Using this we can pass the branch names' )
    string(name: 'PersonName',  defaultValue: 'Bhaskar Reddy', description: 'This Parameter, will use to pass the persona name')
    }
    stages {
        stage('CheckoutCode') {
            steps {
               git branch:"${params.BranchName}" , credentialsId: '9aad10da-e742-413a-a2f6-ce6a8b007f70', url: 'https://github.com/MithunTechnologiesDevOps/maven-web-application.git'
             sh "echo The persona name is: ${params.PersonName}"
             }
        }
    }
}

