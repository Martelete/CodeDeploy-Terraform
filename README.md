## How to create a Website in GitHub and deploy via CodeDeploy AWS and Terraform

1. Create a Sample Website on Github:

- Your repository
- New
- GitHub Pages - set to Master Branch
- Select Themes at your choice (once you back to main page, make sure you have deleted index.html to reproduce the new theme)
- Clone your repository 

2. You can also create a sample Application via AWS and push to your repository:

# In this example I'm using ```US-EAST-1``` as default region. If you want to use different region, just update the section ```//aws-codedeploy-```region```/ as you desired.

```- aws s3 cp s3://aws-codedeploy-us-east-1/samples/latest/SampleApp_Linux.zip . 
- unzip SampleApp_Linux.zip
- rm SampleApp_Linux.zip
- git add .
- git commit -m "Added sample app"
- git push -u origin master```

3. By using CodeDeploy, you can now provision an instance/create application and deployment group and deploy the application to the instance using Terraform scripts.

- In your local machine, go to the folder where the repository was cloned. To deploy via Terraform, open the folder ```terraform-website``` and execute those commands:

### Markdown

```markdown
# To initialize a Terraform working directory
terraform init 

# Generate and show execution plan
terraform plan 

# Builds or changes the infrastructure
terraform apply 
```
