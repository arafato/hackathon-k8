# Alibaba Cloud - K8 Hackathon
Welcome! This is a collection of links and hints that will help you to implement the various scenarios and bonus tasks of our Alibaba Cloud Kubernetes Hackathon. 
Each section below is dedicated to one of the core scenarios. Each of these can be extended with the bonus tasks.
So most combinations are possible: 2B, 2C, 1A, 3D, etc.

Each section will list a couple of resources, links, and services we recommend to use to accomplish the individual scnearios and bonus task. But always feel free to find your own way!

# Core Scenarios
## 1 - Simple serverless cross-region deployment pipeline
1. You'll need a Github (or BitBucket, Private Gitlab) project with a working Dockerfile that contains an app or a service that provides some sort of web interface. The [Kuard](https://github.com/kubernetes-up-and-running/kuard) project might be a good idea to start with for example. 

2. A Managed Kubernetes Cluster on Alibaba Cloud in *Shanghai* (`cn-shanghai`) region. Check out our documentation at https://www.alibabacloud.com/help/doc-detail/95108.htm on how to create a cluster through the web console. Check out https://www.alibabacloud.com/help/doc-detail/86378.htm for information on how to configure `kubectl` to access your cluster.<br> 
**HINT**: You can also use [Alibaba Cloud Shell](https://www.alibabacloud.com/help/doc-detail/90256.htm) to have a pre-configured shell that let's you instantly work with `kubectl`. 

3. An existing Kubernetes Deployment object in your cluster (you need to create it by yourself!) that allows you to create a trigger for a redeployment. This trigger can then be used by your container registry (see 4.).
4. An [Alibaba Cloud Container Registry](https://www.alibabacloud.com/help/doc-detail/60945.htm) with the right build and trigger configuration. Make sure to pull from the VPC-endpoint to save on outbound internet bandwidth. Check out our documentation at https://www.alibabacloud.com/help/doc-detail/60997.htm

## 2 - Reliable geo-redundant serverless cross-region deployment pipeline
1. You'll need a Github (or BitBucket, Private Gitlab) project with a working Dockerfile that contains an app or a service that provides some sort of web interface. The [Kuard](https://github.com/kubernetes-up-and-running/kuard) project might be a good idea to start with for example.

2. A Managed Kubernetes Cluster on Alibaba Cloud in *Shanghai* (`cn-shanghai`) region. Check out our documentation at https://www.alibabacloud.com/help/doc-detail/95108.htm on how to create a cluster through the web console. Check out https://www.alibabacloud.com/help/doc-detail/86378.htm for information on how to configure `kubectl` to access your cluster.<br> 
**HINT**: You can also use [Alibaba Cloud Shell](https://www.alibabacloud.com/help/doc-detail/90256.htm) to have a pre-configured shell that let's you instantly work with `kubectl`. 

3. An existing Kubernetes Deployment object in your cluster (you need to create it by yourself!) that allows you to create a trigger for a redeployment. This trigger can then be used by your container registry (see 4.).

4. You will need two Alibaba Cloud Container Registries (ACR) *Enterprise Edition Basic Version* for cross-region image replication over our private backbone network: one in our *UK* (`eu-west-1`) region, one in our *Shanghai* (`cn-shanghai`) region.
Make sure to configure two different features:
    - the build and trigger configuration for both the *UK* and *Shanghai* based registries. The build will be done in UK, while the deployment will be done from *Shanghai*. Make sure to pull from the VPC-endpoint to save on outbound internet bandwidth. Check out our documentation at https://www.alibabacloud.com/help/doc-detail/60997.htm
    - the image replication from *UK* to *Shanghai*. No documentation available yet. Find your own way in the web console or ask Alibaba Cloud staff on-site.

## 3 - Reliable and private cross-region deployment with Gitlab and CEN
TODO

# Bonus Tasks
## A - Branching Workflow Support
TODO
## B - Reduce cost with Serverless K8 / Virtual Kubelets
TODO
## C - Observability: Integration with Cloud Monitoring services
TODO
## D - Use P2P Acceleration to increase download efficiency of images
TODO

# Did you know...?
- that you can use [Alibaba Cloud Shell](https://www.alibabacloud.com/help/doc-detail/90256.htm) and launch it with a pre-configured version of `kubectl`? See below screenshot on where to find this nice feature:
![alt text](https://github.com/arafato/hackathon-k8/raw/master/img/k8-cloudshell.png "Cloud Shell")

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

