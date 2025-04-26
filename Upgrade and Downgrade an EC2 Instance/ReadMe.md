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





