---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Secure Hybrid Access to Amazon S3 using VPC Endpoints

#### Overview

This workshop focuses on how to access **Amazon S3** privately from AWS workloads and a simulated on-premises environment by using **VPC Endpoints**. The lab helps demonstrate why private connectivity is important when workloads need to reach AWS services without sending traffic through the public internet.

**AWS PrivateLink** provides private connectivity between VPCs, supported AWS services, and on-premises networks. In this workshop, two endpoint patterns are used:

* **Gateway VPC Endpoint:** Used for private access from resources inside a VPC to Amazon S3 through route table configuration.
* **Interface VPC Endpoint:** Used for private access through endpoint network interfaces and DNS resolution, suitable for more advanced or hybrid connectivity scenarios.

Through the lab, I practiced deploying the environment, creating endpoints, testing S3 access, reviewing endpoint policies, checking DNS behavior, and cleaning up resources after completion.

#### Content

1. [Workshop overview](5.1-Workshop-overview/)
2. [Prerequiste](5.2-Prerequiste/)
3. [Access S3 from VPC](5.3-S3-vpc/)
4. [Access S3 from On-premises](5.4-S3-onprem/)
5. [VPC Endpoint Policies (Bonus)](5.5-Policy/)
6. [Clean up](5.6-Cleanup/)
