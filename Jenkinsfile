pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
              sh "aws cloudformation create-stack --stack-name ismaeelt1 --template-body Rootismaeelstack.yml --region 'us-east-1' --parameters ParameterKey=ImageId,ParameterValue=ami-077e31c4939f6a2f3 ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey"
              }
             }
            }
            }aws cloudformation create-stack --stack-name ismaeelt1 --template-body file://Rootismaeelstack.yml --region 'us-east-1' --parameters ParameterKey=ImageId,ParameterValue=ami-077e31c4939f6a2f3 ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey
