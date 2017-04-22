# Node.js Hello World Application

After connecting your Windows server click "Node.js command prompt" under Node.js folder in Start menu. If you didn't install Node.js, you can install it by reading [How to Install Node.js on Windows Server?](http://dogukandemir.com/en/how-to-install-node-js-on-windows-server/) post and then you can run "Node.js command prompt".

In "Node.js command prompt" screen, you can create your first application with the following commands. So what are the meanings of these commands?

![Node.js Hello World](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/en/nodejs-hello-world-application/images/npm-init.png)



For those who do not know how to use command prompts, I want to explain 2 commands I use on the screen, regardless of the Node.js command prompt.

cd: change directory
mkdir: make directory

"cd C:\" command will change your current directory to main directory of C driver.
"mkdir nodejs" command will create a new folder inside current folder.

Once you have created the C:\nodejs\helloworld directory and go to this directory, you can run the npm package builder to create a new Node.js application using the command "npm init". Package builder will ask you some informations respectively name, version, description, entry point, test command, git repository, keywords, author and license. You can create your application with default values (values inside paranthesis) with pressing enter key. I just change description and author fields. Once you have completed the information, you can create your application by checking the preview of your package.json file and pressing the enter key.

"echo console.log("hello world"); > index.js" command will create a file named index.js inside your current directory and writes "console.log("hello world");" into index.js file. The index.js value in this command must be the same as the entry point value. Finally, when you run your application with the "node index" command, you will see "hello world" text which you print it on the screen with "console.log" code line.

Congratulations, you have run your first application after installing Node.js in your Windows server on AWS. Next blog post will be about how to access this application from outside of the server via browser.