# cloudformation-templates

export AWS_PROFILE=<aws-profile> | --profile

aws cloudformation validate-template --template-body file://./<stack>.yml

aws cloudformation create-stack --stack-name <stack_name> --template-body file://./<stack>.yml --parameters file://./params.json

watch -n1 'aws cloudformation describe-stacks --stack-name <stack_name> | grep StackStatus'

# Update(s)
aws cloudformation update-stack --stack-name <stack_name> --template-body file://./<stack>.yml --parameters file://./params.json

# Delete
aws cloudformation delete-stack --stack-name <stack_name>
