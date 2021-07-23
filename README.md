# Vocareum
# to create the stack for an EC2 without a KeyName

aws cloudformation create-stack --stack-name wpvc01 --template-body file://Vocareum/WordPress.yaml --parameters ParameterKey=DBName,ParameterValue=wordpressdb ParameterKey=DBPassword,ParameterValue=password ParameterKey=DBRootPassword,ParameterValue=password ParameterKey=DBUser,ParameterValue=masteruser


# to create the stack for an EC2 with a KeyName
aws cloudformation create-stack --stack-name wpvc01 --template-body file://Vocareum/WordPress.yaml --parameters ParameterKey=KeyName,ParameterValue=wordpressstack01 ParameterKey=DBName,ParameterValue=wordpressdb ParameterKey=DBPassword,ParameterValue=password ParameterKey=DBRootPassword,ParameterValue=password ParameterKey=DBUser,ParameterValue=masteruser


# to delete a stack
aws cloudformation delete-stack --stack-name wordpress04


# to list all EC2 instances
aws ec2 describe-instances

# to list all running EC2 instances. The state of the instance (pending | running | shutting-down | terminated | stopping | stopped )
aws ec2 describe-instances --filters Name=instance-state-name,Values=running
