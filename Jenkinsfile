String logicalenv= 'qa'
pipeline {
    agent any

    stages {
        stage('Show Files') {
            steps {
//               withCredentials([string(credentialsId: 'AccessKeyID', variable: 'AWS_ACCESS_KEY_ID'), string(credentialsId: 'SecretAccessKey', variable: 'AWS_SECRET_ACCESS_KEY')]) {
//               String scriptOutput = sh(script:'''aws cloudformation create-stack --stack-name ismaeelawsclitest2 --template-body file://Rootismaeelstack.yml --region "us-east-1" --parameters ParameterKey=ImageId,ParameterValue=ami-0c2b8ca1dad447f8a ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyBucketName,ParameterValue=ismaeels3bucketfornestedstack   ParameterKey=PrivateSubnet1CIDR,ParameterValue=10.0.2.0/24  ParameterKey=PublicSubnet1CIDR,ParameterValue=10.0.1.0/24 ParameterKey=PublicSubnet2CIDR,ParameterValue=10.0.3.0/24 ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16''' +logicalenv,returnStdout: true).trim()
//               def scriptOutput = sh(script:''' ls -la ''',returnStatus: true).trim()
              script {
                def output = sh(returnStdout: true, script: 'pwd')

                echo ${output}
    //               sh 'echo "scriptOutput: ${scriptOutput}"'
//                   sh 'echo "hy there is ismaeel haider" '
              } 
                //             }
//               String scriptOutput = sh(script:'aws cloudformation create-stack --stack-name ismaeelawsclitest2 --template-body file://Rootismaeelstack.yml --region "us-east-1" --parameters ParameterKey=ImageId,ParameterValue=ami-0c2b8ca1dad447f8a ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyBucketName,ParameterValue=ismaeels3bucketfornestedstack   ParameterKey=PrivateSubnet1CIDR,ParameterValue=10.0.2.0/24  ParameterKey=PublicSubnet1CIDR,ParameterValue=10.0.1.0/24 ParameterKey=PublicSubnet2CIDR,ParameterValue=10.0.3.0/24 ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16',returnStdout: true).trim()
//                 steps {
//               echo "scriptOutput: ${scriptOutput}"  
//               sh '''
//                 echo "ismaeel haier"
//               '''
//               sh '''
//                 echo "${myflie}"
//               '''                
                
         }
        }
            
            
            
            
            }
        }





