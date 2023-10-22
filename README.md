# Prereq for password manager 
- Create AWS account https://aws.amazon.com/
- Download Virtual Box https://www.virtualbox.org/wiki/Downloads
- Install ubuntu virtual machine https://ubuntu.com/download/desktop
- Name cheap register domain https://www.namecheap.com/







# Getting started with password manager
- Go to passbolt https://www.passbolt.com/
- On prem install
- Free
- Select AWS and deploy
  ![image](https://github.com/ali0999109/Password/assets/145396907/78014f0a-12b9-4107-8aba-37f833c03e19)







# Setting up password manager hosted in AWS
- Continue to subscribe
- Continue to config
- Continue to launch
- Security group settings > Create new based on seller settings > add name and description > Save
- Key pair settings > create a key pair in EC2 > Actions > import key pair >
- Go to ubuntu virtual machine > command line > ssh-keygen > enter > Y > Enter > cat ~/.ssh/id_rsa.pub > copy and paste your key into AWS
  ![image](https://github.com/ali0999109/Password/assets/145396907/fb185b05-5389-49b9-86ee-1c5f370ad85d)

- Import key pair
- Go back to keypair settings > select the key pair you created
- Launch
- go to ec2 > click on the PublicIPV4 address to open pass bolt config wizard
  ![image](https://github.com/ali0999109/Password/assets/145396907/20070f90-631e-4fba-a886-851e9c04ae9f)





# Password manager HTTPS Config
- Click on get started
- Go to name cheap buy a domain name > Advanced DNS > A record > Value @ > Host IpV4 address of the EC2 instance
  ![image](https://github.com/ali0999109/Password/assets/145396907/8057983a-784a-4ed8-ab44-cb716ce870b0)

-Go to ubuntu VM and paste your ec2 ip address in the command prompt  ssh admin@ipaddress > yes
![image](https://github.com/ali0999109/Password/assets/145396907/16182272-265a-4570-a0f9-45c8630fe9a4)

- Type in > sudo nano /etc/nginx/sites-enabled/nginx-passbolt.conf
- type in your domain name for server name
  ![image](https://github.com/ali0999109/Password/assets/145396907/7eacf0e0-bf16-48d0-8e26-2d4abcfc4c3a)
- press control and x
- click yes
- type in sudo dpkg-reconfigure passbolt-ce-server
- MySQL no
- Nginx Yes
- Auto
- Admin@Your domain name
- enter
  








# Password manager config in AWS
- Go to passbolt config
- Start config
- Next
- Server keys > add server name & email
- Emails > add your details to sender name, sender email, and SMTP host click next
- first, last name, and username
- Thats it






#


