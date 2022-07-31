# Udacity *Advanced Cloud DevOps Nanodegree Program*
## 2- Deploy Infrastructure as Code (*IAC*)

## Project 2 : Deploy a high-availability web app using CloudFormation

### Description
Create a Launch Configuration in order to deploy four servers, two located in each of your private subnets.  
The launch configuration will be used by an auto-scaling group.  
You'll need two vCPUs and at least 4GB of RAM. The Operating System to be used is Ubuntu 18.  
So, choose an Instance size and Machine Image (AMI) that best fits this spec.  
Be sure to allocate at least 10GB of disk space so that you don't run into issues.

### Architecture
![](https://i.imgur.com/VUVy3sU.png)

### How to run the project:

1. Network infrastructure stack Usage:
```shell
./create.sh netstackName network.yml network-parameters.json
```

2. After step 1 has been completed successfully, run the services infrastructure stack Usage:

```shell
./create.sh serverstackName server.yml server-parameters.json
 ```

 3. Updating the network infrastructure stack Usage:
 
```shell
./update.sh netstackName network.yml network-parameters.json
```
4. Updating the services infrastructure stack Usage:

```shell
./update.sh serverstackName server.yml server-parameters.json
```


# WebApp URL:
http://serve-WebAp-1HESZ7MAZT598-158522272.us-east-1.elb.amazonaws.com