# My-Learnings
EC2 Technical gufthugu
{TG}
EC2-ELASTIC COMPUTE CLOUD
Amazon Elastic Compute Cloud (Amazon EC2) provides on-demand, scalable computing capacity in the Amazon Web Services (AWS) Cloud. 
It Allows you to Rent Virtual servers, known as instances, to run applications and Services.
Using Amazon EC2 reduces hardware costs so you can develop and deploy applications faster. 
You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. 
Amazon EC2 enables you to Scale up or Scale down the instances.
Amazon EC2 having two storage opts i.e 
1. EBS & 
2. Instances Storage.
PRE Configure templates are avalible known as Amazon Machine Image.
By default, When you Create an EC2 account with amazon, your amazon is linked to a maximum of 20 instances per EC2 Region with two default high I/O instances
This limit applies only to running instances. Stopped, hibernated, or pending instances do not count against this limit.

{U}
EC2 = Elastic Compute Cloud = Infrastructure as a Service
• It mainly consists in the capability of:
• Renting virtual machines (EC2)
• Storing data on virtual drives (EBS)
• Distributing load across machines (ELB)
• Scaling the services using an auto-scaling group (ASG)

{U}
EC2 sizing & configuration options
• Operating System (OS): Linux, Windows or Mac OS
• How much compute power & cores (CPU)
• How much random-access memory (RAM)
• How much storage space:
• Network-attached (EBS & EFS)
• hardware (EC2 Instance Store)
• Network card: speed of the card, Public IP address
• Firewall rules: security group
• Bootstrap script (configure at first launch): EC2 User Data

{U}
EC2 User Data
• It is possible to bootstrap our instances using an EC2 User data script.
• bootstrapping means launching commands when a machine starts
• That script is only run once at the instance first start
• EC2 user data is used to automate boot tasks such as:
• Installing updates 
• Installing software
• Downloading common files from the internet
• Anything you can think of
• The EC2 User Data Script runs with the root user

{U} 
EC2 Instance Types - Overview
• You can use different types of EC2 instances that are optimised for different use cases (https://aws.amazon.com/ec2/instance-types/)
• AWS has the following naming convention
m5.2xlarge
• m: instance class
• 5: generation (AWS improves them over time)
• 2xlarge: size within the instance class

{TG}
Types of EC2 Instances:
General Purpose --- Balanced Memory & CPU
Compute Optimized ---More CPU than RAM
Memory Optimized ---- More CPU
Accelerated Computing /GPU -----Graphics Optimized
Storage Optimized --- Low latency
High Memory Optimized ----High RAM, Nitro System(uses spl type of Hypervisor)
__________________________________________________________________________________
Amazon EC2 provides a wide selection of instance types optimized to fit different use cases. Instance types comprise varying combinations of CPU, memory, storage, and networking capacity and give you the flexibility to choose the appropriate mix of resources for your applications. Each instance type includes one or more instance sizes, allowing you to scale your resources to the requirements of your target workload.

Here's a comprehensive overview of AWS EC2 instance types, including definitions, suitable use cases, configuration ranges (vCPU, RAM, storage), and other pertinent details, arranged by instance family.

### 1. *General Purpose Instances*
#### Definitions:
General Purpose instances provide a balance of compute, memory, and networking resources. They can be used for a variety of workloads.

#### Series:
- *T4g, T3, T3a, T2:* Burstable performance instances with a baseline level of CPU performance.
- *M7g, M6g, M6i, M5, M5a, M5n, M4:* Balance of compute, memory, and networking resources.

#### Use Cases:
- Web servers
- Application servers
- Small to medium databases
- Development and test environments

Configuration Range:
- *vCPUs:* Up to 96 vCPUs
- *RAM:* Up to 384 GiB
- *Storage:* EBS-optimized (EBS-only)

### 2. *Compute Optimized Instances*
#### Definitions:
Compute Optimized instances are ideal for compute-bound applications that benefit from high-performance processors.

#### Series:
- *C7g, C6g, C6i, C6a, C5, C5a, C5n, C4*

#### Use Cases:
- High-performance web servers
- Scientific modeling
- Batch processing
- Machine learning inference

#### Configuration Range:
- *vCPUs:* Up to 128 vCPUs
- *RAM:* Up to 256 GiB
- *Storage:* EBS-optimized (EBS-only)

### 3. *Memory Optimized Instances*
#### Definitions:
Memory Optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.

#### Series:
- *R7g, R6g, R6i, R6a, R5, R5a, R5n, R4*
- *X2idn, X2iedn, X1, X1e:* High memory instances for large-scale, memory-intensive applications.
- *u-6tb1.metal, u-9tb1.metal, u-12tb1.metal:* High memory bare metal instances for SAP HANA and other memory-intensive applications.

#### Use Cases:
- High-performance databases
- In-memory caches
- Real-time big data analytics

#### Configuration Range:
- *vCPUs:* Up to 128 vCPUs
- *RAM:* Up to 24 TiB
- *Storage:* EBS-optimized (EBS-only)

### 4. *Accelerated Computing Instances*
#### Definitions:
Accelerated Computing instances use hardware accelerators, or co-processors, to perform functions such as floating-point number calculations, graphics processing, or data pattern matching.

#### Series:
- *P4d, P3, P2:* Instances with GPUs for general-purpose GPU computing.
- *Inf1:* Instances for machine learning inference.
- *G5, G4ad, G4dn, G3:* Graphics-intensive workloads.

#### Use Cases:
- Machine learning training and inference
- Computational fluid dynamics
- Molecular modeling
- Rendering and transcoding video

#### Configuration Range:
- *vCPUs:* Up to 96 vCPUs
- *RAM:* Up to 1.1 TiB
- *Storage:* EBS-optimized (EBS-only), local NVMe SSDs available on certain instances

### 5. *Storage Optimized Instances*
#### Definitions:
Storage Optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage.

#### Series:
- *I4i, I3en, I3:* High I/O instances.
- *D3, D2:* Dense storage instances.
- *H1:* Instances for high disk throughput.

#### Use Cases:
- NoSQL databases (e.g., Cassandra, MongoDB)
- Data warehousing
- Distributed file systems

#### Configuration Range:
- *vCPUs:* Up to 96 vCPUs
- *RAM:* Up to 1.5 TiB
- *Storage:* Up to 60 TB of NVMe SSD or HDD

### Additional Information:
- *EBS-Optimized:* All instances are EBS-optimized by default, providing dedicated throughput to EBS volumes.
- *Networking:* Enhanced networking with up to 100 Gbps throughput on certain instances.
- *Bare Metal:* Available for certain instance types, providing direct access to hardware for workloads that require non-virtualized environments.

### Summary
This summary provides a high-level overview of the different types of AWS EC2 instances, along with their series, use cases, and configuration ranges. This is essential knowledge for AWS certification and helps in choosing the right instance type for specific workloads.

General Purpose Instances:
General Purpose instances Provide a Balance of Compute , Memory and Networking Resources , and can be used for a Variety of workloads
Instances Available in four sizes – Nano,Small, Medium, Large
A series
(A1-Instances)
A1- instances are ideally suited for scale-out workloads that are supported by the ARM Ecosystem
M series
T  series 




__________________________________________________________________________________
{CG}
When to Use Each Instance Type:
•	General Purpose: Suitable for a wide range of workloads where the balance of compute, memory, and networking is important but not specialized.
•	Compute Optimized: Ideal for compute-intensive applications that require high-performance processors.
•	Memory Optimized: Best for memory-intensive applications that require high RAM capacity and fast memory performance.
•	Storage Optimized: Designed for applications that require high I/O performance and large amounts of local storage.
•	Accelerated Computing: Used for applications that benefit from GPU or FPGA acceleration, such as machine learning, gaming, and video rendering.
•	FPGA Instances: Specifically for applications that require hardware acceleration using Field Programmable Gate Arrays (FPGAs).

{G}
 


