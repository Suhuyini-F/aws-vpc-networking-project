## Project Overview
Designed and configured a custom AWS network to demonstrate practical cloud networking, infrastructure deployment and security configuration.

## AWS Architecture

```mermaid
flowchart TB
    Internet((Internet))
    subgraph VPC["Custom VPC — 10.0.0.0/16"]
        IGW["Internet Gateway"]
        subgraph Public["Public Subnet"]
            PublicEC2["Public EC2"]
            NAT["NAT Gateway"]
        end
        subgraph Private["Private Subnet"]
            PrivateEC2["Private EC2"]
        end
        IGW --> PublicEC2
        PublicEC2 --> NAT
        NAT --> IGW
        PrivateEC2 --> NAT
    end
    Internet <--> IGW

## Infrastructure Built
- Custom VPC with a public and private subnet.
- Internet Gateway for public internet connectivity.
- NAT Gateway with an Elastic IP for private subnet outbound access.
- Separate route tables for public and private traffic.
- Public and private EC2 instances.
- Security Groups to control inbound and outbound traffic.

## Technical Skills Demonstrated
- AWS VPC and subnet configuration.
- IPv4 addressing and CIDR notation.
- Public and private network architecture.
- Internet Gateway and NAT Gateway configuration.
- Route table management and traffic routing.
- EC2 deployment and SSH connectivity.
- Network security using Security Groups.

## Technologies Used
AWS VPC, EC2, Internet Gateway, NAT Gateway, Elastic IP, Route Tables and Security Groups.

**Implementation:** AWS Management Console

## Project Status
Core infrastructure and both EC2 instances have been created. Network connectivity testing and validation are ongoing.
