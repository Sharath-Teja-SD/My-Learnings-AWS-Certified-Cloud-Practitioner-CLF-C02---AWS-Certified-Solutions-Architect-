# 📘 My Learnings: AWS EC2 – Elastic Compute Cloud

**Certifications Covered:**
- AWS Certified Cloud Practitioner (CLF-C02)
- AWS Certified Solutions Architect – Associate (SAA-C03)

---

## ☁️ EC2 - Elastic Compute Cloud

Amazon Elastic Compute Cloud (Amazon EC2) provides on-demand, scalable computing capacity in the AWS Cloud.  
It allows you to **rent virtual servers (instances)** to run applications and services.

### 🔹 Key Benefits:
- Reduces hardware costs
- Launch as many/few instances as needed
- Configure security, networking, storage
- Easily scale up/down
- Pre-configured templates: **Amazon Machine Images (AMI)**
- Default limit: **20 running instances per EC2 Region** (excluding stopped, hibernated, or pending)

---

## 🏗️ EC2 = Infrastructure as a Service (IaaS)

Main capabilities:
- Renting virtual machines (EC2)
- Storing data (EBS)
- Load balancing (ELB)
- Auto-scaling (ASG)

---

## ⚙️ EC2 Configuration Options

- Operating System (Linux, Windows, Mac)
- CPU: Compute power & cores
- RAM: Memory capacity
- Storage:
  - Network-attached (EBS, EFS)
  - Local (Instance Store)
- Network card: Speed, Public IP
- Security: Security Groups (Firewall Rules)
- **Bootstrap Script:** EC2 User Data

---

## 📜 EC2 User Data

- Automates tasks on first launch (bootstrapping)
- Runs as **root** user
- Example tasks:
  - Install updates
  - Install software
  - Download files

---

## 🧱 EC2 Instance Types - Overview

AWS provides different instance types optimized for specific workloads.  
**Naming Convention Example:** `m5.2xlarge`
- `m`: Instance class
- `5`: Generation
- `2xlarge`: Size

---

## 📊 EC2 Instance Families

### 1. General Purpose
**Balanced Compute, Memory, Networking**

| Series | Description |
|--------|-------------|
| T4g, T3, T3a, T2 | Burstable performance |
| M7g, M6g, M5, M5a, M5n, M4 | Balanced for general workloads |

**Use Cases:** Web servers, app servers, small DBs, dev/test  
**Config Range:** Up to 96 vCPUs, 384 GiB RAM, EBS only

---

### 2. Compute Optimized
**More CPU than RAM**

| Series | Description |
|--------|-------------|
| C7g, C6g, C6i, C6a, C5, C5a, C5n, C4 | High-performance CPUs |

**Use Cases:** High-perf web servers, ML inference, scientific modeling  
**Config Range:** Up to 128 vCPUs, 256 GiB RAM, EBS only

---

### 3. Memory Optimized
**More RAM for in-memory data processing**

| Series | Description |
|--------|-------------|
| R7g, R6g, R6i, R5, R5a, R4 | High memory |
| X2idn, X1e, u-6tb1.metal | SAP HANA & memory-heavy apps |

**Use Cases:** High-perf DBs, real-time analytics, caches  
**Config Range:** Up to 128 vCPUs, 24 TiB RAM, EBS only

---

### 4. Accelerated Computing
**For GPU, ML, HPC workloads**

| Series | Description |
|--------|-------------|
| P4d, P3, P2 | GPU computing |
| Inf1 | ML inference |
| G5, G4dn, G3 | Graphics-intensive apps |

**Use Cases:** ML training/inference, CFD, rendering  
**Config Range:** Up to 96 vCPUs, 1.1 TiB RAM, EBS + NVMe

---

### 5. Storage Optimized
**For high I/O and local storage needs**

| Series | Description |
|--------|-------------|
| I4i, I3en, I3 | High IOPS |
| D3, D2 | Dense HDD |
| H1 | High throughput disk |

**Use Cases:** NoSQL DBs, DW, distributed storage  
**Config Range:** Up to 96 vCPUs, 1.5 TiB RAM, up to 60 TB storage

---

## 📌 Additional Notes

- **EBS-Optimized:** All instances are EBS-optimized by default
- **Networking:** Up to 100 Gbps enhanced networking
- **Bare Metal:** Direct hardware access for some instance types

---

## 🧭 When to Use Each Instance Type

| Instance Type        | Use Case |
|----------------------|----------|
| General Purpose      | Balanced workload needs |
| Compute Optimized    | High-performance CPU tasks |
| Memory Optimized     | In-memory DBs, caching |
| Storage Optimized    | High IOPS, large local storage |
| Accelerated Computing| GPU, ML, video rendering |
| FPGA                 | Hardware acceleration apps |

---

## 🧠 Quick Recap

- EC2 = Elastic Compute in AWS Cloud
- Offers scalable, on-demand compute power
- Choose instance types based on workload needs
- Automate with EC2 User Data
- Understand instance types to pass AWS certifications and make better infra decisions

---

## 🔗 Resources

- [EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/)
- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2)

