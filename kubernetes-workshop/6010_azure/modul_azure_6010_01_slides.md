## Kubernetes on Azure

---

## Motivation for using Kubernetes on Azure

### 

There are a number of point to factor into your decision to use the K8s services
available in the Azure Public Cloud today.

### Team readiness
* Have you containerized any of your workloads?
* Is there a CI/CD Platform in use in your Organization

### Cloud Strategy
* Does your organization have a cloud strategy?
* Are you already using other Azure backed services (ie. Office 365,
  Microsoft Dynamic CRM)?

### Multi-Cloud
* Are you already running parts of your container workloads in other public
  clouds like AWS or GKE?
* Would you like to be able to react to changes in the pricing model on
  existing clouds by shifting loads to where you get a better deal?

### Known and trusted vendor
* Do you already have an existing relationship with Microsoft?
* *No one ever got fired for picking Microsoft*

--- 

## Kubernetes Services

Most modern services on Azure are backed by Kubernetes

### High-Level

Azure PaaS offerings

* Container Instances
* Managed PostgreSQL/MariaDB on Azure
* NoSQL as a Service

### Low-Level

* ACS (GA)
* AKS (Public Preview)
* OpenShift on Azure (Public Preview)

### DIY

* acs-engine (tooling used to build ACS/AKS)
* raw VMs (Bring you own K8s)

---

## Azure PaaS

### 

* Turnkey tooling enabling PaaS usage of Azure
* Everything managed by Microsoft
* Fewer customizing options compared to Low-Level and DIY solutions

### Cloud Native Databases on Azure

* Basic NoSQL databases like CosmosDB that offer Cassandra-/MongoDB-as-a-Service
* Relational databases (MS SQL, PostgreSQL, MySQL)

These are usually built using the same Kubernetes Technology used by other
offerings.

### Container Instances

* Allow you to use the Azure API to deploy you container workloads.
* Additional Abstraction layer between your Deploy and Kubernetes
* *Almost* Serverless
* Can be tied into an AKS Cluster by way of a virtual-kubelet or the Open Service Broker for Azure

---

## ACS/AKS Kubernetes Clusters

### ACS

* Initial Kubernetes on Azure available in GA
* Installs a well integrated Kubernetes Cluster on Azure
* Allows full access to Kubernetes master and nodes

### AKS

* Master node(s) managed by Microsoft
* You only pay for nodes
* Accessing the master directly (ie. for debugging) is not supported
* Accessing nodes is possible but needs some configuration

### Openshift on Azure

* For fans of a fully managed Stack from RedHat
* Uses the same tooling also used by ACS/AKS

### Y U NO SuSE CAP

* Fastest way to CloudFoundry PaaS on AKS
* Contact your SuSe TAM and/or your Microsoft Account Manager

---

## DIY

### acs-engine

* Tooling used to build ACS/AKS Clusters
* Can also be used directly
* See what is on the roadmap by watching the repository on GitHub
* Great for hacker, not so great if you need/want support by Microsoft
* Community support on GitHub works and is awesome

### Bring your own Kubernetes

* Use tools like Terraform to provision VMs and deploy Kubernetes on top
* Other tools like Rancher2 offer turnkey solutions for standing up clusters
  on Azure.

###

---

## What the Azure

### 

* Azure Resource Manager (ARM)
* Azure Active Directory (AAD)

* Subscriptions
* Resource Groups
* Service Principals / Application Thingies in AD

