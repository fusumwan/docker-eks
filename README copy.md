# deploy-to-eks-using-github-actions
1. Create an EKS Cluster using this command:

Run the aws cloudformation delete-stack Command:

Use the following command to delete the stack:

aws cloudformation delete-stack --stack-name eksctl-dockereks-cluster --region ap-southeast-2

Monitor the Deletion Process:

You can check the status of the stack deletion with the following command:

aws cloudformation describe-stacks --stack-name eksctl-dockereks-cluster --region ap-southeast-2


 

eksctl delete cluster --region=ap-southeast-2 --name=dockereks

eksctl create cluster --name dockereks --region ap-southeast-2 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2

2. Then create .github folder and then create workflow folder inside .github folder 
3. create file with .yml extension and write the workflow code
4. Create a github repository 
5. Create secrets in github repo
        Go to settings of repo
        click on secrets and variables
6. Test application by getting the dns name and going to a web browser

Clean up: Run: eksctl delete cluster --name dockereks


=============================================================
ECR

879409995620.dkr.ecr.ap-southeast-2.amazonaws.com/dockereks

============================================================

aws eks describe-cluster --name dockereks --region ap-southeast-2 --query "cluster.endpoint" --output text

https://F6AFC9C25CE164F038E11249D2C45231.gr7.ap-southeast-2.eks.amazonaws.com

F6AFC9C25CE164F038E11249D2C45231.gr7.ap-southeast-2.eks.amazonaws.com


=============================================================================
Type command to get website url.

kubectl get service

a00a0af03710c4306b6d20fa39baa6cc-257399999.ap-southeast-2.elb.amazonaws.com