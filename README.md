# Azure Three Tier Web Architecture Workshop

## Description: 
This workshop is a hands-on walk through of a three-tier web architecture in Azure. We will be manually creating the necessary network, security, app, and database components and configurations in order to run this architecture in an available and scalable manner.

## Audience:
Although this is an introductory level workshop, it is intended for those who have a technical role. The assumption is that you have at least some foundational aws knowledge around VPC, EC2, RDS, S3, ELB and the AWS Console.  

## Pre-requisites:
1. An Azure account. 
1. IDE or text editor of your choice.

## Architecture Overview
![Architecture Diagram]([https://github.com/aws-samples/aws-three-tier-web-architecture-workshop/blob/main/application-code/web-tier/src/assets/3TierArch.png](https://github.com/jstanesic/azure-three-tier-web-architecture-workshop/blob/main/application-code/web-tier/src/assets/3TierArch.png))

In this architecture, a public-facing Load Balancer or Application Gateway forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Azure Database for MySQL flexible server and returns it to our web tier. Load balancing, health checks and VM scale sets are created at each layer to maintain the availability of this architecture.

## Original workshop
This Azure Three Tier Web Architecture is based on [AWS Three Tier Web Architecture](https://catalog.us-east-1.prod.workshops.aws/workshops/85cd2bb2-7f79-4e96-bdee-8078e469752a/en-US)
and [Red Hat Linux 3-Tier Solution on Azure](https://learn.microsoft.com/en-us/samples/azure/azure-quickstart-templates/rhel-3tier-iaas/)

## Workshop Instructions:
Original instructions are available at [AWS Three Tier Web Architecture](https://catalog.us-east-1.prod.workshops.aws/workshops/85cd2bb2-7f79-4e96-bdee-8078e469752a/en-US)

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

