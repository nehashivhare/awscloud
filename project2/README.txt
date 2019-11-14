#Create Role named Udagram-EC2-Role for EC2 instances:
aws iam create-role --role-name Udagram-EC2-Role --assume-role-policy-document file://final-project-policy.json

#Attach AmazonS3ReadOnlyAccess to this role
aws iam attach-role-policy --role-name Udagram-EC2-Role --policy-arn arn:aws:iam::aws:policy/AmazonS3ReadOnlyAccess

