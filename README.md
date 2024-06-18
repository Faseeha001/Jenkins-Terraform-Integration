# Automate Infrastructure setup using Terraform and Jenkins Pipeline
## Pre-requisites:
1. Jenkins is up and running
2. Terraform is installed in Jenkins
3.Terraform files already created in your SCM
4. Make sure you have necessary IAM role created with right policy and attached to Jenkins EC2 instance. see below for the steps to create IAM role.

## 1) Create a new Jenkins Pipeline
## 2) Add parameters to the pipeline

    Click checkbox - This project is parameterized, choose Choice Parameter
    
    <img width="243" alt="image" src="https://github.com/Faseeha001/Jenkins-Terraform-Integration/assets/169563689/5bc69c86-6486-4c42-9d2f-a6c9dabbedc5">
    
    Enter name as action
    type apply and enter and type destroy as choices as it is shown below(it should be in two lines)
   apply destroy
   <img width="780" alt="image" src="https://github.com/Faseeha001/Terraform_Jenkins/assets/169563689/e17b7f4f-e6b4-42a6-8d08-0333bdf444f4">

## configuration
<img width="679" alt="image" src="https://github.com/Faseeha001/Terraform_Jenkins/assets/169563689/7d0ea777-5a4e-4d43-8cdc-072a249263c9">

## Go to Pipeline section

1. Add below pipeline code and modify per your GitHub repo configuration.
pipeline script :
<img width="614" alt="image" src="https://github.com/Faseeha001/Terraform_Jenkins/assets/169563689/c41ff38d-2b2f-49cf-9dd6-697b266996c1">
2. Click on Build with Parameters and choose apply to build the infrastructure or choose destroy if you like to destroy the infrastructure you have built.
3. Click on Build
4. Now you should see the console output if you choose apply.
 console output with action Apply :

<img width="731" alt="image" src="https://github.com/Faseeha001/Terraform_Jenkins/assets/169563689/a20c5887-dc5f-4731-b1a3-53bad4e6b98f">
<img width="754" alt="image" src="https://github.com/Faseeha001/Terraform_Jenkins/assets/169563689/111f6e4e-ed2e-40a3-be9f-630fd7fdeb46">
<img width="694" alt="image" src="https://github.com/Faseeha001/Terraform_Jenkins/assets/169563689/24412a87-ea5b-4f12-b56a-d349c4349ee6">

4:Login to AWS console, you should see the new EC2 instance created.
E2C instance: 
<img width="802" alt="image" src="https://github.com/Faseeha001/Terraform_Jenkins/assets/169563689/5f76a5a2-5bc1-471a-83bb-497b8d059e9c">

Destroy :

<img width="609" alt="image" src="https://github.com/Faseeha001/Jenkins-Terraform-Integration/assets/169563689/b9f2c36c-c129-4588-92a7-fc9f436c8d37">
1) Ec2 dashboard after destroy action
<img width="848" alt="image" src="https://github.com/Faseeha001/Jenkins-Terraform-Integration/assets/169563689/3328e584-dad8-49bb-8fd6-3438dd80e563">
2) Console output with action destroy :
<img width="687" alt="image" src="https://github.com/Faseeha001/Jenkins-Terraform-Integration/assets/169563689/43e13973-f6c0-483e-9052-88c71bcfae46">
<img width="692" alt="image" src="https://github.com/Faseeha001/Jenkins-Terraform-Integration/assets/169563689/f363eb6c-1e9b-458d-87db-25aee0b96fbd">
<img width="678" alt="image" src="https://github.com/Faseeha001/Jenkins-Terraform-Integration/assets/169563689/27444858-d0f6-40d3-9751-fd332a0b5d6c">




