pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage ('checking out code') {
            steps {
                git branch: 'main', url: 'https://github.com/gupt28a/demo.git'
            }
        }
        stage ('create ec2') {
            steps {
                sh "aws cloudformation create-stack --stack-name myteststack --template-body file://sampleec2.json"
            }
        }
        
    }
}
