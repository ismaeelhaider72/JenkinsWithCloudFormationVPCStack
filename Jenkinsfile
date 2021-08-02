pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
              withCredentials([string(credentialsId: 'AccessKeyID', variable: 'AWS_ACCESS_KEY_ID'), string(credentialsId: 'AccessKeyID', variable: 'AWS_SECRET_ACCESS_KEY')]) {
              sh "sudo aws cloudformation create-stack --stack-name ismaeelt1 --template-body file://Rootismaeelstack.yml --region 'us-east-1' --parameters ParameterKey=ImageId,ParameterValue=ami-0c2b8ca1dad447f8a ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey"
                              
                    
                    
                    // some block
                }                
                
//               sh "sudo mkdir /home/ismaeel/ismaeeltest1"
//               sh "sudo aws cloudformation create-stack --stack-name ismaeelt1 --template-body file://Rootismaeelstack.yml --region 'us-east-1' --parameters ParameterKey=ImageId,ParameterValue=ami-077e31c4939f6a2f3 ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey"
              
            }
             }
            }
            }
