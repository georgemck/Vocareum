# Vocareum
# to create the stack for an EC2 without a KeyName

aws cloudformation create-stack --stack-name wpvc01 --template-body file://Vocareum/WordPress.yaml --parameters ParameterKey=DBName,ParameterValue=wordpressdb ParameterKey=DBPassword,ParameterValue=password ParameterKey=DBRootPassword,ParameterValue=password ParameterKey=DBUser,ParameterValue=masteruser


# to create the stack for an EC2 with a KeyName
aws cloudformation create-stack --stack-name wpvc01 --template-body file://Vocareum/WordPress.yaml --parameters ParameterKey=KeyName,ParameterValue=wordpressstack01 ParameterKey=DBName,ParameterValue=wordpressdb ParameterKey=DBPassword,ParameterValue=password ParameterKey=DBRootPassword,ParameterValue=password ParameterKey=DBUser,ParameterValue=masteruser


# to delete a stack
aws cloudformation delete-stack --stack-name wordpress04
