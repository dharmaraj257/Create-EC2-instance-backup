
# Create An AWS EC2 Backup and Launch a new Instance using Backup AMI.

launch a new EC2 instance. for backup create a snapshot, and add EBS volume for backup. Create AMI using the existing running EC2 instance Which you want to backup. Using created Backup AMI launch a new instance.

###  Step 1: Launch the Ec2 instance

1. Give a name to Ec2 Instance WordPress.

2. Select OS Ubuntu 22.04 and Instance type t2.micro.

3. Create and download the key pair.

4. Select Vpc create a Security group and add ports, SSH 22, HTTP 80, and HTTPS 443 allowing them to anywhere.

5. Click Launch Instance

&nbsp;
   

![ec1](https://github.com/dharmaraj257/Deploy-WordPress-website-on-Ec2/assets/100831265/8c7e8389-5adf-4347-8a74-bbdf4603cc95)



&nbsp;

### Step 2: Create  a snapshot
1. The Volumes section should open and select volume.

2. Click Action and select Create Snapshot.

3. Give a description and click Create Snapshot.

&nbsp;

![Screenshot (127)](https://github.com/dharmaraj257/Deploy-WordPress-website-on-Ec2/assets/100831265/0c7e4f0e-f82b-4901-8861-71b5db66c181)

&nbsp;

4. Open the snapshot section now you can see the latest created snapshot.

5. Select snapshot press action and create volume from a snapshot, Configure the volume details(volume type, six, IOPS, availability Zone, tags).

6. Then, Click Create Volume for the new volume created. which you can later be added to the AWS EC2 instance of your choice.

&nbsp;

![Screenshot (128)](https://github.com/dharmaraj257/Deploy-WordPress-website-on-Ec2/assets/100831265/9ee2456e-76cd-4aea-9b35-24906a8f9ee7)

&nbsp;

### Step 3: Create a new AMI

1. Select the running  instance to create a backup.

2.Click Actions>Image>Create Image.

3. You can specify the image name, add the Image description, enable/disable reboot after the AMI creation, and configure instance volumes.

4. Click Create Image.

&nbsp;

![ec3](https://github.com/dharmaraj257/Deploy-WordPress-website-on-Ec2/assets/100831265/4dc542b9-4819-4c83-9802-915285de7413)

&nbsp;

### Step 4: launch new Ec2 inastance Using latestes created AMI.

1. Click launch new instance and give a name.

2. In Application and OS Images, Click  My AMIS options and select the latest created AMI (Ubuntu-Ec2-backup).
   
&nbsp;

![Screenshot (129)](https://github.com/dharmaraj257/Deploy-WordPress-website-on-Ec2/assets/100831265/ac188ee5-8ac8-4474-8d21-aa0a0516b90b)

&nbsp;

3. Create and download the key pair.

4. Select Vpc create a Security group and add ports, SSH 22, HTTP 80, and HTTPS 443 allowing them to go anywhere.

5. Click Launch Instance.
   
&nbsp;

![ec2](https://github.com/dharmaraj257/Deploy-WordPress-website-on-Ec2/assets/100831265/59841bd5-9e6e-40be-b533-d6709cf0df13)
