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
### Task 1: Setup Visual Studio Code  
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

