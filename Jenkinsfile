 pipeline {
    agent any

    stages {

stage ('Release') {
      steps {
                script {
                    def apply = true
                    def status = null
                    withCredentials([string(credentialsId: 'AccessKeyID', variable: 'AWS_ACCESS_KEY_ID'), string(credentialsId: 'SecretAccessKey', variable: 'AWS_SECRET_ACCESS_KEY')]) {
                    try {
                            status = sh(script: "aws cloudformation describe-stacks --stack-name ismaeelawsclitest2 \
                                --query Stacks[0].StackStatus --output text ", returnStdout: true)
                            apply = true
                            sh "echo this is describe create parts"
                    } catch (err) {
                            apply = false
                            sh 'echo Creating ismaeelawsclitest2....'
                            sh "aws cloudformation validate-template --template-body ile://Rootismaeelstack.yml "
                            sh "aws cloudformation create-stack --stack-name  ismaeelawsclitest2 --template-body file://Rootismaeelstack.yml --parameters file://params.json "
                            sh "aws cloudformation describe-stack-events --stack-name ismaeelawsclitest2\
                                            --query 'StackEvents[].[{Resource:LogicalResourceId,Status:ResourceStatus,Reason:ResourceStatusReason}]' \
                                            --output table "
                    }
                    if (apply) {
                            try {
                                    sh "aws cloudformation update-stack --stack-name ismaeelawsclitest2 --template-body file://Rootismaeelstack.yml --parameters file://params.json "
                            } catch (error) {
                                    sh "echo Finished create/update - no updates to be performed"
                                    echo "stack failed"
                                    sh 'exit 1'
                            }
                    }
                    sh "aws cloudformation wait stack-update-complete --stack-name ismaeelawsclitest2 "
                                     
                    sh "echo Finished create/update successfully!"
                 }                     
                }
      }
        }
                                        
        }
     }

