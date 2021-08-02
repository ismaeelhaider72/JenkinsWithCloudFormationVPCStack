pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
              withCredentials([string(credentialsId: 'AccessKeyID', variable: 'AWS_ACCESS_KEY_ID'), string(credentialsId: 'SecretAccessKey', variable: 'AWS_SECRET_ACCESS_KEY')]) {
                sh ''' aws cloudformation create-stack --stack-name ismaeelawsclitest2 --template-body file://Rootismaeelstack.yml --region 'us-east-1' --parameters ParameterKey=ImageId,ParameterValue=ami-0c2b8ca1dad447f8f ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyBucketName,ParameterValue=ismaeels3bucketfornestedstack   ParameterKey=PrivateSubnet1CIDR,ParameterValue=10.0.2.0/24  ParameterKey=PublicSubnet1CIDR,ParameterValue=10.0.1.0/24 ParameterKey=PublicSubnet2CIDR,ParameterValue=10.0.3.0/24 ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16 '''
                  // some block
                }                
                
//                withCredentials([string(credentialsId: 'AccessKeyID', variable: 'aws_access_key_id'), string(credentialsId: 'SecretAccessKey', variable: 'aws_secret_access_key')]) {
//                  sh ''' aws cloudformation create-stack --stack-name ismaeelawsclitest2 --template-body file://Rootismaeelstack.yml --region 'us-east-1' --parameters ParameterKey=ImageId,ParameterValue=ami-0c2b8ca1dad447f8a ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyBucketName,ParameterValue=ismaeels3bucketfornestedstack   ParameterKey=PrivateSubnet1CIDR,ParameterValue=10.0.2.0/24  ParameterKey=PublicSubnet1CIDR,ParameterValue=10.0.1.0/24 ParameterKey=PublicSubnet2CIDR,ParameterValue=10.0.3.0/24 ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16 '''
//                 }             
                
//               sh "sudo mkdir /home/ismaeel/ismaeeltest1"
//               sh "sudo aws cloudformation create-stack --stack-name ismaeelt1 --template-body file://Rootismaeelstack.yml --region 'us-east-1' --parameters ParameterKey=ImageId,ParameterValue=ami-077e31c4939f6a2f3 ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey"
              
            }
             }
            }
            }
