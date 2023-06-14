# Udagram (cloudformation)

![Diagram](./Project%20IAC%20Diagram.png)

Final project for the **Deploy Infrastructure as Code (IAC)** section of Udacity **Cloud DevOps Engineer** course.

Run the following commands to create stacks:

**1-network.yaml**
```bash
aws cloudformation create-stack --stack-name network --template-body file://stacks/1-network.yaml
```

**2-servers.yaml**
```bash
aws cloudformation create-stack --stack-name server --template-body file://stacks/2-servers.yaml
```

From the web console wait for the `network` stack to complete before creating the `server` stack.

In the `server` stack if you provide a `BastionHostKeyName` parameter, a bastion server will be created that enables SSH access to private servers.
