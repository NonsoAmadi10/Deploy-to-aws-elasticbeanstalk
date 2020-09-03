# Deploy-to-aws-elasticbeanstalk
- A simple demonstration of how to deploy a node js application to the aws Elastic Beanstalk

### Tools

- Node JS

- awsebcli

- Linux(OS)

## To deploy to Elastic Beanstalk using the cli
 - Install the cli:
    - Ubuntu/Debian: 
    ` apt-get awsebcli `
    - Redhat:
    `yum install awsebcli`

    - Pip(python packge manager):
        `pip install awsebcli --upgrade --user `

- Configure the cli:
    - Run  `eb init`
    - Next, provide your access key and secret key so that the EB CLI can manage resources for you. Access keys are created in the AWS Identity and Access Management console. 
    - An application in Elastic Beanstalk is a resource that contains a set of application versions (source), environments, and saved configurations that are associated with a single web application. Each time you deploy your source code to Elastic Beanstalk using the EB CLI, a new application version is created and added to the list.

- Deploying to beanstalk using the cli:
    - Ensure your node_modules are added to the gitignore file

    - Run ` eb init --platform node.js --region us-east-2 `

    - Remember the region could be any aws data center region of your choice

    - Run `eb create  node-express`
    
    - After every process is done, you can open the file using:
     `eb open`