# AWS Infrastructure Automation Project

## Overview

This project automates the deployment of a highly available AWS infrastructure using **Python (boto3)**. It provisions a multi-tier architecture including **VPC, Subnets, Security Groups, EC2 Instances, NAT Gateway, Load Balancer, Auto Scaling Group, and RDS Database**.

## Features

- **Automated VPC creation** with public and private subnets
- **Security groups setup** for controlled access
- **EC2 instances deployment** in private subnets
- **NAT Gateway & Internet Gateway** for internet access
- **Application Load Balancer** for high availability
- **Auto Scaling Group** for dynamic instance scaling
- **Multi-AZ RDS deployment** for database redundancy

## Prerequisites

- An **AWS account** with administrative privileges
- **Python 3.7+** installed
- **boto3** library installed (`pip install boto3`)
- An **IAM user** with permissions to create AWS resources
  
## Installation

Clone the repository:

```bash
 git clone https://github.com/SaaedT/AWS-Infrastructure-Automation.git
 cd AWS-Infrastructure-Automation
```

Install dependencies:

```bash
pip install boto3
```

## How to Run

1. Configure your AWS credentials using AWS CLI:
   ```bash
   aws configure
   ```
2. Run the script:
   ```bash
   python test.py
   ```
3. The script will output the created resources' details, such as **VPC ID, Subnet IDs, Security Group IDs, Load Balancer DNS, and RDS Endpoint**.

### Running in an IDE

- You can run the script directly from **VS Code** or **PyCharm** by opening the project and executing `test.py`.
- Alternatively, run the script from the **Terminal / Command Prompt** using:
  ```bash
  python test.py
  ```

## Execution Steps

The script executes the following steps:

1. **Create a VPC**
2. **Create public and private subnets**
3. **Attach an Internet Gateway** to the VPC
4. **Setup route tables and NAT Gateway**
5. **Create security groups** for instances, load balancer, and database
6. **Launch EC2 instances** in private subnets with Apache installed
7. **Deploy an Application Load Balancer**
8. **Configure Auto Scaling Group**
9. **Setup an RDS Multi-AZ Database**

## Expected Output

After successful execution, you should see output similar to:

```bash
New VPC has been created successfully with id vpc-xxxxxx
Public Subnets have been created successfully , their ids are subnet-xxxxxx and subnet-xxxxxx
Private Subnets have been created successfully , their ids are subnet-xxxxxx and subnet-xxxxxx
...
Application Load Balancer is up and available now
RDS Instance is up and available now
```

(Full output can be found in the **`Project1_Expected_Output.txt`** file.) 
!(Project1_Expecetd_Output.txt)

## Improvements & Future Enhancements

- Add **Logging and Error Handling** for better debugging
- Implement **CI/CD pipeline** for automated deployment
- Integrate **CloudWatch Monitoring** for resource tracking
- Include **Terraform or CloudFormation** to define infrastructure as code (IaC)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

[Mo Saeed Tello](https://github.com/SaaedT)
