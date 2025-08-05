# Setup Kubernetes on Amazon EKS

# kubernetes cluster setup with AWS EKS

# pre-requisites:
one EC2-instance with below requirements
1. t2.medium (2 CPUs & 2GB RAM)
2. linux os
3. 10GB storage 

# AWS EKS Setup 
1. Setup kubectl 
 a. Download kubectl version  from (https://kubernetes.io/docs/tasks/tools/install-kubectl-linux)
 b. Grant execution permissions to kubectl executable 
 c. Move kubectl onto /usr/local/bin
 d. Test that your kubectl installation was successful
 
  ##Kubectl.sh
  curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.33.0/2025-05-01/bin/linux/amd64/kubectl
  chmod +x ./kubectl
  mv ./kubectl /usr/local/bin 
  kubectl version --client

2. EKS SetUp
 a. Download and extract the latest release  
 b. Move the extracted binary to /usr/local/bin 
 c. Test that your eksclt installation was successful  
 
  ##EKS.sh
  curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"
  tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz
  chmod +x /tmp/eksctl
  sudo mv /tmp/eksctl /usr/local/bin
  eksctl version

curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
   sudo mv /tmp/eksctl /usr/local/bin
   eksctl version

3. Create an IAM Role and attache it to EC2 instance  
   IAM   
   EC2   
   VPC    
   CloudFormation
   if any other requires means you want to add in attach policy or add administration policy.

4. Create your cluster and nodes 
   sh
   eksctl create cluster --name cluster-name  --region region-name --node-type instance-type --nodes-min 2 --nodes-max 4 --zones <AZ-1>,<AZ-2> 
      (or)
   eksctl create cluster --name cluster-name  \
   --region region-name \
   --node-type instance-type \
   --nodes-min 2 \
   --nodes-max 2 \ 
   --zones <AZ-1>,<AZ-2>

 example:
   eksctl create cluster --name sanjay \
   --region us-east-1 \
   --node-type t2.micro

5. To delete the EKS clsuter 
   sh 
   eksctl delete cluster sanjay --region us-east-1

6. Validate your cluster using by creating by checking nodes and by creating a pod 
   sh
   kubectl get nodes




