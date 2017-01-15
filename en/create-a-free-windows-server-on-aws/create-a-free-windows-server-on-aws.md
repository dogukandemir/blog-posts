# Create a Free Windows Server on AWS

If you don't have an AWS account, you can create it by reading my [Create an AWS Account](http://dogukandemir.com/en/create-an-aws-account/) post. IF you create your account, login to your account, go to [https://console.aws.amazon.com](https://console.aws.amazon.com) address and select EC2 under Services.

![Services EC2](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/console-services-compute-ec2.png)



Click "Launch Instance" button under Create Instance panel.

![Launch Instance](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/console-create-instance.png)



In this step choose operating system of your server. In this post we will continue by creating a Windows server. To do this click "Select" button next to "Microsoft Windows Server 2016 Base".

![Microsoft Windows Server 2016 Base](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/windows-server-2016-select-button.png)



Once you have selected t2.micro as our server type, click "Next: Configure Instance Details" button.

![Instance Type](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/instance-type-configure-button.png)



You can click "Next" button without making any changes in "Configure Instance", "Add Storage" and "Add Tags" steps.

Note: You can make changes to the settings in these steps, but you should not exceed your needs when making your selections. Otherwise, your credit card may be charged.



We will make some changes in "Configure Security Group" step. To provide RDP, HTTP and HTTPS access to our server, we need to add these rules (RDP attached by default) first. In addition, you can add 8080 and 3000 ports to use for development. If you want to access your server from anywhere, you need to select "Anywhere" as "Source" property. If you want to restrict access, you can enter IP address by CIDR ([Classless Inter-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)) notation after selecting "Custom" or "My IP". After you have done your settings, click "Review and Launch" button.

![Configure Security Group](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/security-group.png)



In the last step, click "Launch" button after review your server properties.

![Launch Instance](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/review-instance-launch.png)



In order to connect to the server, you need to have a key pair file. To create a key pair file click "Create a new key pair", give a name in "Key pair name" field and click "Download Key Pair" button. Key pair dosyasını oluşturmak için "Create a new key pair" seçip "Key pair name" alanına istediğiniz bir isim verdikten sonra "Download Key Pair" butonuna tıklayarak dosyayı indirmeniz gerekiyor. After download of your file, click the "Launch Instances" button.

Note: You need to save key pair file where you have access and you should not lose your key pair file. You can download this file only the first time you create it. There is no panel you can download later.

![Create a new key pair](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/key-pair-launch-instances.png)



Congratulations, your server is in preparation phase. Click the "View Instances" button to see status of your server.

[![View Instance](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/view-instances.png)](https://console.aws.amazon.com/ec2/v2/home?#Instances:sort=instanceId)



It takes a few minutes to be ready. You can see the state of your server in "Instance State" field.

![Instance State](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/view-instances-instance-state.png)



You can give a name to your server to easily find it when you have lots of servers. When you hover "Name" field, there will be a pencil icon. Click pencil icon and give a name to your server.

![Edit Name](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/view-instances-edit-name-button.png) ![Name Edit](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/create-a-free-windows-server-on-aws/images/view-instances-edit-name-done-button.png)



Congratulations. You successfully created a Windows server. Next blog post will be about how to connect this server remotely.