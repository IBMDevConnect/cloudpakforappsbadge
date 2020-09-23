# Setting up developer workspace and running a simple Node.js application

#### The below document helps to setup the developer project workspace in Code Ready provided IDE

**Step 1:**  Login to the Open shift Cluster through the Web console, where the Code ready workspace is setup.

**Step 2:**  Access the Code Ready Workspace through the appropriate Code ready workspace URL that would have been shared.

**Step 3:** If you are accessing it for the first time you need register as the registration page will be shown.  Ensure your user name should have strictly follow .(character allowed are 0-9, a-z and hypen in between), even if default values are displace. Ensure you provide details regarding username, Email, First name and Last name (If SSO is not configured, you need provide the password as well. From the second you will be directly taken to workspace User interface in step 4

**Step 4:**  Navigate to the default page codeready workspace as loaded in the below picture

![Cloud Login](images/Picture1.png)

**Step 5:**  You can create the workspace as shown in the step 4  by selecting one of the template stacks displace. Alternatively navigate to the Custom Workspace and select the NodeJS Express option for the Devfile

![Cloud Login](images/Picture2.png)

**Step 6:** Click on create and open button. Workspace will start loading. This may take few minutes as the Container and plug-ins related to the stack has be created and deployment.  Once the Workspace is created  the welcome will be displayed as depicted below

![Cloud Login](images/Picture5.png)

**Step 7:** Open the terminal by selecting terminal from menu:

![Cloud Login](images/Picture6.png)

**Step 8:** Click on open the terminal and select maven

![Cloud Login](images/Picture7.png)

**Step 9:** Clone the project

```
git clone https://github.com/IBMDevConnect/node-hello
```

**Step 10:** Get into the directory

```
cd node-hello
```

**Step 11:** Run the application

```
node index.js
```

**Step 12:** There will be a pop-up, please click on Open Link

![Cloud Login](images/Pic.png)

**Step 13:** You should be able to get the output as shown below:

![Cloud Login](images/Output.png)

Congratulations! You have completed this workshop!
