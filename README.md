# cloudformation-templates

export AWS_PROFILE=<aws-profile>

aws cloudformation validate-template --template-body file://./wpt.yml

aws cloudformation create-stack --stack-name <env>-ws03 --template-body file://./wpt.yml --parameters file://./params.json

watch -n1 'aws cloudformation describe-stacks --stack-name <env>-ws03 | grep StackStatus'

# Update(s)
aws cloudformation update-stack --stack-name <env>-ws03 --template-body file://./wpt.yml --parameters file://./params.json

# Delete
aws cloudformation delete-stack --stack-name <env>-ws03
