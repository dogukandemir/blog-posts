# Connect to Windows Server on AWS

If you don't create a Windows Server on AWS, you can create it by reading my [Create a Free Windows Server on AWS](http://dogukandemir.com/en/create-a-free-windows-server-on-aws/) post. If you have created your server, click "Connect" button after selecting server which named "Windows Server 2016" under "Instances" page.

![Connect](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/connect-to-windows-server-on-aws/images/connect-button.png)



In "Connect To Your Instance" panel after clicking "Download Remote Desktop File" button to download .rdp file, click "Get Password" button to get "Administrator" password.

![Connect To Your Instance](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/connect-to-windows-server-on-aws/images/connect-to-your-instance.png)



In this step, we need key-pair file which we created in previous blog post. My key-pair file name is "Windows2016Server.pem", that's why it asks us to choose Windows2016Server.pem file. After file selection, click "Decrypt Password" button.

![Decrypt Password](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/connect-to-windows-server-on-aws/images/connect-to-your-instance-get-password.png)



You can see password of your "Administrator" user.

![Username Password](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/connect-to-windows-server-on-aws/images/username-password.png)



When you open .rdp file which we just downloaded, click "Connect" button to bypass that warning. Copy password which you see in "Password" section, paste it as password of your "Administrator" user and click "OK" button. You can bypass warning about certificate by clicking "Yes" button.

![Enter Your Credentials](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/connect-to-windows-server-on-aws/images/enter-your-credentials.png)



When you connect to your server, you can see details of your server in upper right corner of the screen.

![Server Details](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/connect-to-windows-server-on-aws/images/server-details.png)



Congratulations. You have successfully connected to your Windows server. Next blog post will be about how to install node.js to this server.