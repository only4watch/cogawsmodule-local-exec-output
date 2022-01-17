# cogawsmodule-local-exec-output
we need to locate key-pair from ec2instance dashboard
download and use it to connect bastion hostfirst
ssh -i terraform-key.pem ec2-user@bastion public ipaddress 
ls -ltr /tmp 
you cant fine .PEM file
*****IMP INSTRUCTION************
now locate to GIT WORKSPACE
mkdir -p private-key/terraform-key.pem
copy terraform-key pair content to private-key/terraform-key.pem
*****************************************************************
git pull (from this code)

terraform init

terraform apply

then we can see .pem file copied from [private-key/terrafrom-key.pem should created manually in workspace of this repo ] to bastion host under /tmp location

now we need to login bastion host with help of .pem file

ssh -i terraform-key.pem ec2-user@bastion public ipaddress 

locate to /tmp

ls -ltr bastionhoste server

you can see .pem file copied

now next step is copy private ipaddres of ec2 server 

cd tmp/ ssh -i terraform-key.pem ec2-user@private ipaddres of ec2
now you can connect to PRIVATE IPADDRESS of another EC2HOST


*** please note private-key/terraform-key.pem will not be check-in due to gitignore 

