# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
For this particular app, it was an easy decision for me to go with App service. Here are are the points influeced my decision 
1. For this particalar excersize, I wouldn't need compute power more than what app service can offer. 
2. Azure has automated deloyment option to deploy code using github actions to App service. 
3. Azure app service has free tier that I can use for deploying a web app

All the above points made me choose app service over virtual machine

| Feature     | App Service   | Virtual Machine |
| ----------- | ----------- |     -----------   |
| Costs       | App service has free version that can be utilized for this kind of excersize       | VM doesn't have free tier and there is minimum cost per month for month to utilize it
| Scalability   | App Service can be auto scaled based on the needs. | VM can be scaled using scale sets
| Availability   | No service level agreement will be provided for free tier. Apps running on subscription level will be provided with 99.95% availability  | VM gets availability from 95% and up based on various factors like availability zones, sets, etc
| Workflow   | App service supports various deployment options like github actions, AZ devops pipelines, etc      | VM also supports similar features like instant deployment from github, az devops, etc. No Built in support for application updates


Based on above factors I have picked App service for this excersize. Costs - App service has a free tier that I was able to utilize for deploying the application. Scalability - It was not a big concern for me as it is a test application. Availability - Even though, there was no SLA available for free tier of the app service, I was able to test the application. Workflow - I was able to create github action to deploy code from github to app service.

On contrary to my above points, I would switch to virtual machine as my option in case below situations 

1. If I need full access to OS and the softwares installed on the server as VM give me the control to install the required services for the app that I would like run on the machine
2. App service has limitation on scalability when it comes to number of cores and RAM. VM can be scaled a lot more than app service.
3. When cost is not a problem to maintain and scale the application then VM is a great option for app environment.

