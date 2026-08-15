Azure-Hub-Spoke-Terraform

A Terraform automation project that deploys a Hub-and-Spoke Network Topology on Microsoft Azure. This project provisions all network infrastructure using Infrastructure as Code, demonstrating enterprise-level network design and automated deployment skills.

Architecture Overview

The hub-and-spoke topology connects a central hub virtual network to two spoke virtual networks through VNet peering. All traffic routes through the hub, simulating how enterprises isolate workloads while maintaining centralized connectivity.

```mermaid
graph TD
 HUB["🔷 hub-vnet 10.0.0.0/16"]
 S1["🔹 spoke1-vnet 10.1.0.0/16"]
 S2["🔹 spoke2-vnet 10.2.0.0/16"]

 HUB -- "spoke1-to-hub | Connected | Fully Synchronized" --- S1
 HUB -- "spoke2-to-hub | Connected | Fully Synchronized" --- S2
```

Technologies Used

- Microsoft Azure
- Terraform (Infrastructure as Code)
- Azure Virtual Networks (VNet)
- VNet Peering
- Azure Resource Groups

Infrastructure Components

Resource Group

Resource Group (screenshots/01-resource-group-terraform.png)
<img width="1067" height="429" alt="01-resource-group-terraform" src="https://github.com/user-attachments/assets/88984b0d-86b0-4680-a32f-3d7c75f42dac" />


Hub Virtual Network

Hub VNet (screenshots/02-hub-vnet-terraform.png)
<img width="1075" height="542" alt="02-hub-vnet-terraform" src="https://github.com/user-attachments/assets/9352bf1e-1117-49ec-8e0a-8dd6d5268fcb" />


Spoke 1 Virtual Network

Spoke1 VNet (screenshots/03-spoke1-vnet-terraform.png)
<img width="1077" height="522" alt="03-spoke1-vnet-terraform" src="https://github.com/user-attachments/assets/9af21375-0c14-4c5b-8d8e-3db1c40aefe9" />


Spoke 2 Virtual Network

Spoke2 VNet (screenshots/04-spoke2-vnet-terraform.png)

<img width="1069" height="533" alt="04-spoke2-vnet-terraform" src="https://github.com/user-attachments/assets/aba59329-f6d0-4559-93ce-055c81a94e73" />


Hub VNet Peerings

Hub VNet Peerings (screenshots/05-hub-vnet-peerings-terraform.png)
<img width="1105" height="364" alt="05-hub-vnet-peerings-terraform" src="https://github.com/user-attachments/assets/6ac22c11-8db5-41ea-af7e-fd484c940df6" />


Deployment

```
git clone https://github.com/maxmagnac/azure-hub-spoke-terraform.git
cd azure-hub-spoke-terraform
terraform init
terraform plan
terraform apply
```

Related Projects

- azure-hub-spoke-network (https://github.com/maxmagnac/azure-hub-spoke-network) - Manual deployment of the same Hub-and-Spoke topology

Author: Maurrin Carter
