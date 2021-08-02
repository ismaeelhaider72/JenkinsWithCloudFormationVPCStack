def stderrfile = 'stderr.out'
pipeline {
    agent {
        label '!windows'
    }

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
        stage('Show Files') {
            environment {
              MY_FILES = sh(script: 'aws cloudformation describe-stacks  --stack-name ismaeelawsclitest6 --template-body file://Rootismaeelstack.yml --region 'us-east-1' --parameters ParameterKey=ImageId,ParameterValue=ami-0c2b8ca1dad447f8a ParameterKey=MyKeyName,ParameterValue=ismaeelhaiderUbunterPCKey ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=MyBucketName,ParameterValue=ismaeels3bucketfornestedstack   ParameterKey=PrivateSubnet1CIDR,ParameterValue=10.0.2.0/24  ParameterKey=PublicSubnet1CIDR,ParameterValue=10.0.1.0/24 ParameterKey=PublicSubnet2CIDR,ParameterValue=10.0.3.0/24 ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16 , returnStdout: true)
            }
            steps {
              sh '''
                echo "$MY_FILES"
              '''
            }
        }
            
            
            
            
            }
        }





