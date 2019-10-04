# Alibaba Cloud - K8 Hackathon
Welcome! This is a collection of links and hints that will help you to implement the various scenarios and bonus tasks of our Alibaba Cloud Kubernetes Hackathon. 
Each section below is dedicated to one of the core scenarios. Each of these can be extended with the bonus tasks.
So most combinations are possible: 2B, 2C, 1A, 3D, etc.

# Core Scenarios
## 1 - Simple serverless cross-region deployment pipeline
For this scenario you will need three things:
1. Github (or BitBucket, Private Gitlab) project with a working Dockerfile. The [Kuard](https://github.com/kubernetes-up-and-running/kuard) project might be a good idea to start with for example. 
2. A Managed Kubernetes Cluster on Alibaba Cloud in *Shanghai* region. Check out our documentation at https://www.alibabacloud.com/help/doc-detail/95108.htm on how to create a cluster through the web console. Check out https://www.alibabacloud.com/help/doc-detail/86378.htm for information on how to configure `kubectl` to access your cluster. 

**HINT**: You can also use [Alibaba Cloud Shell](https://www.alibabacloud.com/help/doc-detail/90256.htm) to have a pre-configured shell that let's you instantly work with `kubectl`. 

## 2 - Reliable geo-redundant serverless cross-region deployment pipeline
TODO
## 3 - Reliable and private cross-region deployment with Gitlab and CEN
TODO

# Bonus Tasks
## A - Supporting Branching Workflow
TODO
## B - Reduce cost with Serverless K8 / Virtual Kubelets
TODO
## C - Observability: Integration with Cloud Monitoring services
TODO
## D - Use P2P Acceleration to increase download efficiency of images
TODO

# Did you know...?
- that you can use [Alibaba Cloud Shell](https://www.alibabacloud.com/help/doc-detail/90256.htm) and launch it with a pre-configured version of `kubectl`? See below screenshot on where to find this nice feature:
![alt text](https://github.com/arafato/hackathon-k8/raw/master/imgk8-cloudshell.png "Cloud Shell")

# Tools and General Links
This section contains a list of general resources and links to tools you may find useful to accomplish the tasks.

**Kubectl** - CLI for controlling the K8 cluster manager<br>
https://kubernetes.io/docs/tasks/tools/install-kubectl/

**Docker Desktop for Mac / Windows** - The Docker CLI and runtime<br>
https://hub.docker.com/?overlay=onboarding

**Aliyun CLI** - The official Alibaba Cloud CLI<br>
https://github.com/aliyun/aliyun-cli

**Terraform for Alibaba Cloud** - Documentation of the Alibaba Cloud Resource Provider<br> 
https://www.terraform.io/docs/providers/alicloud/

**Alibaba Cloud Documentation** - Official Alibaba Cloud documentation<br>
https://www.alibabacloud.com/help

