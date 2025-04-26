## Objective
- Provision infrastructure on AWS using Terraform commands and configurations.  
- Use Terraform attributes like variables, outputs and providers.  
- Gain Hands-On experience of Terraform workflow commands i.e., terraform init, terraform plan, terraform apply, and terraform destroy.  
- Differentiate between **AWS CloudFormation** and **HashiCorp Terraform.**  

## Prerequsites  
Knowledge of AWS Services  
- [AWS Management Console](https://aws.amazon.com/console/)  
- Amazon EC2  
- Basic Terraform commands.  

## Scenario:  
This project guides through the steps on how to upgrade and downgrade the EC2 instance type when the traffic changes using Terraform.  

## Architecture Diagram: 

![terraform architecture diagram ec2 upgrade downgrade](https://github.com/user-attachments/assets/103025e4-e6a1-4149-b944-70b907523be6)

## Task Details:  
1. Sign in to [AWS Management Console](https://aws.amazon.com/console/)  
2. Setup / Download [Visual Studio Code](https://code.visualstudio.com)
3. Create a Variable File.
4. Launch an EC2 in main.tf file.
5. Create an output file.
6. Confirm the installation of Terraform by checking the version.
7. Apply Terraform configuration.
8. Check the resources in [AWS Management Console](https://aws.amazon.com/console/)
9. Upgrading Instance type from t2.micro to t2.medium
10. Downgrading Instance type from t2.medium to t2.micro
11. Delete AWS Resources.

## Steps:  
### Step 1: Setup Visual Studio Code  
1. Open the Visual Studio Code.
2. If you have already installed using Visual Studio Code, open a new window.
3. A new window will open a new file and release notes page. Close the Release Notes tab.
4. Open Terminal by selecting View from the Menu bar and choose Terminal
5. Once the terminal is ready, navigate to the Desktop: cd Desktop
6. Create a new folder by running: mkdir task_042025
7. Change the present working directory to to the newly create by running: cd task_042025
8. ![mkdir vscode](https://github.com/user-attachments/assets/a1cc54f7-f9c8-43ec-8855-73965c2e23a0)
9. Get the location of the current working directory by running : pwd
10. Note down the location, as we will use the same location.
11. In Visual Studio, click on the first icon **Explorer** on the left sidebar.
12. Click on **Open Folder** and navigate to the location of folder task_042025  
![vs code open folder](https://github.com/user-attachments/assets/4d02c226-cdda-4d24-9fcd-d31cadbe5045)
13. Authorise the folder ![vscode trust folder](https://github.com/user-attachments/assets/fa2a7fd6-3bca-45da-bbfb-3c3f093d65bd)
14. Visual studio Code is now ready to use.

### Step 2: Create a variable file
In this section, we will create variable files where we will declare all the global variables with a short description and a default value.  
1. To create a variable file, exampand the folder task_042025 and click on the New File icon to add the file.  
2. Name the file as variables.tf and press Enter to save it.  
3. Note: Don't change the location of the new file, keep it default, i.e., inside the task_042025 folder.  
4. Type the below contents in variables.tf file as per screenshot and save the file by pressing ctrl + S.
5. ![variable ss](https://github.com/user-attachments/assets/d7c94373-13bc-42eb-aea1-a7fe4fff4e97)
6. Create another New File in task_042025 folder and name it terraform.tfvars
7. ![terraform tfvars](https://github.com/user-attachments/assets/215ddee7-7a01-4654-9991-8942bdb2737c)   

### Step 3: Launch an EC2 Instance in main.tf file  
In this step, we will create a main.tf file where we will add details of the provider and resources.  
1. To create a main.tf file, under the folder task_042025, create a new file and name it main.tf
2. Enter the code as per screen shot below
3. ![main tf](https://github.com/user-attachments/assets/fc2da633-7f54-44bb-b33c-e449240bc834)
4. In the above code, we defined the provider as aws.
5. We now want to tell Terraform to launch an EC2 Instance.
6. To launch an EC2 Instance, write the below content into the main.tf after the provider.
7. ![ec2 launch](https://github.com/user-attachments/assets/e16517f8-8769-4269-b962-c26260843287)
8. This will now launch an Ec2 instance with t2.micro as the instance type.
9. Save the file by pressing Ctrl + S or File - Save.

### Step 4: Create an Output file  
In this step, we will create an output.tf file where we will add details of the provider and resources.  
- In the task_042025 folder, click on the New File icon to add the file.
- Name the file as output.tf and press Enter to save it.
- Write or Paste the below content / code into the output.tf file.
- ![output tf](https://github.com/user-attachments/assets/a5d93522-1e70-4c1f-a8a4-584f3b6c6dc7)
- In the above code, we will extract details of the resources created to confirm that they are created.

### Step 5: Confirm the installation of Terraform by checking the version
- In the Visual Studio Code, open Terminal by selecting View from the Menu bar and choosing Terminal.
- ![accessing terminal](https://github.com/user-attachments/assets/c09a192c-9078-4563-89d5-6f896f1ad099)
- If you are not in the newly created folder, change your working directory by running on the command prompt: cd task_042025
- ![terminal vs code](https://github.com/user-attachments/assets/bcc107ec-6259-4a92-a26a-8ff33a79c58d)
- If you are getting an output as command not found: terraform, this means terraform has not been installed on your system, to Install Terraform, follow the official guide [Download Terraform](https://terraform.io/downloads.html)

### Step 6: Apply Terraform Configurations
- Initialise Terraform by running the following command : **terafform init**  
- ![terraform init command](https://github.com/user-attachments/assets/65800c78-ecb6-4288-8f78-30c2cb22d19f)
- Terraform init checks all the plugin dependencies and downloads them if required, this will then create a deployment plan.  
- To generate the action plans, run the following command : **terraform plan**  
- ![terraform plan](https://github.com/user-attachments/assets/428fe243-cd7b-4db3-814a-b8907bd4f749)
- To create all the resources declared in main.tf configuration file, run the command : **terraform apply**
- Approve the creation of all resources by entering : **yes**  
- ![terrafform apply](https://github.com/user-attachments/assets/26d91cbd-0939-40f5-8e43-23db4d56b218)

### Step 7: Check the resources in AWS Console  
1. Make sure you are in the US East (N.Virginia) us-east-1 region.
2. Navigate to EC2 by clicking on Services on the top, then click on EC2 in the Compute section.
3. Click on the Instances on the left navigation panel. You will then see the Instance has been created successfully.
4. Wait for the status of the EC2 Instance to change to **Running** and the health check status to `check passed.`

### Step 8: Upgrading Instance type from t2.micro to t2.medium  
In this section, we will change the instance type from t2.micro to t2.medium.  
t2.micro which contains 1vCPU, 1GiB memory and 6 CPU credits/hour while t2.medium contains 2 vCPUs, 4GiB memory, and 24 CPU credits/hour.  
1. In Visual Studio Code, open main.tf file  
2. In EC2 code section, update the instance type from t2.micro to t2.medium  
3. ![t2micro](https://github.com/user-attachments/assets/784c8a7c-c1d6-4e16-8cde-af3e471088fa)
4. Save the file by pressing Ctrl + S or File - Save.  
5. ![t2micro status](https://github.com/user-attachments/assets/f4c3dfed-7b74-4e15-a996-0e5a6e0ae30e)
6. To modify the instance, type the following command in the terminal : terraform apply  
7. ![terraform apply t2 medium](https://github.com/user-attachments/assets/f16c5072-03de-40b4-ac1a-61c2b8247810)
8. Approve by entering yes.  
9. ![t2micro status](https://github.com/user-attachments/assets/7d9d67b8-0157-4c40-be5d-a16579f49bbb)
10. Below is the EC2 status change from t2.micro to t2.medium  
11. ![ec2medium](https://github.com/user-attachments/assets/df7a5f40-f159-4d5e-b9f8-6102ed575c75)








