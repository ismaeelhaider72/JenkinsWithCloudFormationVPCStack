pipeline {
    agent any

    stages {
        stage ('Release') {
      steps {
                script {
                    withCredentials([string(credentialsId: 'AccessKeyID', variable: 'AWS_ACCESS_KEY_ID'), string(credentialsId: 'SecretAccessKey', variable: 'AWS_SECRET_ACCESS_KEY')]) {
                    def apply = true
                    def status = null
                    try {
                            status = sh(script: "aws cloudformation describe-stacks --stack-name ismaeelawsclitest2\
                                --query Stacks[0].StackStatus --output text ", returnStdout: true)
                            apply = true
                    } catch (err) {
                            apply = false
                            sh 'echo Creating ismaeelawsclitest2'
                            sh "aws cloudformation validate-template --template-body file://Rootismaeelstack.yml "
                            sh "aws cloudformation create-stack --stack-name  ismaeelawsclitest2 --template-body file://Rootismaeelstack.yml --parameters ParameterKey=ImageId,ParameterValue=ami-0c2b8ca1dad447f8a ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyBucketName,ParameterValue=ismaeels3bucketfornestedstack   ParameterKey=PrivateSubnet1CIDR,ParameterValue=10.0.2.0/24  ParameterKey=PublicSubnet1CIDR,ParameterValue=10.0.1.0/24 ParameterKey=PublicSubnet2CIDR,ParameterValue=10.0.3.0/24 ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16 "
                            sh "aws cloudformation wait stack-create-complete --stack-name ismaeelawsclitest2 "
                            sh "aws cloudformation describe-stack-events --stack-name ismaeelawsclitest2\
                                            --query 'StackEvents[].[{Resource:LogicalResourceId,Status:ResourceStatus,Reason:ResourceStatusReason}]' \
                                            --output table"
                    }
                    if (apply) {
                            try {
                                    sh "echo Stack exists, attempting updating the stack..."
                                    sh "aws cloudformation update-stack --stack-name ismaeelawsclitest2 --template-body file://Rootismaeelstack.yml --parameters ParameterKey=ImageId,ParameterValue=ami-0c2b8ca1dad447f8a ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyBucketName,ParameterValue=ismaeels3bucketfornestedstack   ParameterKey=PrivateSubnet1CIDR,ParameterValue=10.0.2.0/24  ParameterKey=PublicSubnet1CIDR,ParameterValue=10.0.1.0/24 ParameterKey=PublicSubnet2CIDR,ParameterValue=10.0.3.0/24 ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16"
                            } catch (error) {
                                    sh "echo Finished create/update - no updates to be performed"
                            }
                    }
                    sh "echo Finished create/update successfully!"
                }
                    }
      }
   
            
            }
        }
        }
