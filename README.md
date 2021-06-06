[![Python application test with Github Actions](https://github.com/philbier/building-cicd-pipeline/actions/workflows/pythonapp.yml/badge.svg?branch=main)](https://github.com/philbier/building-cicd-pipeline/actions/workflows/pythonapp.yml)

# Building a CI/CD Pipeline


![Set up Azure Cloud Shell](./img/set_up_az_shell.png)

![Continuous Delivery on Azure](./img/cd_on_azure.png)

# Overview
This is the final project for the course "Building a CI/CD pipeline" as part of of the Udacity Cloud DevOps Nanodegree
<TODO: complete this with an overview of your project>

## Project Plan
<TODO: Project Plan

* A link to a Trello board for the project
* A link to a spreadsheet that includes the original and final project plan>

## Instructions

<TODO:  
* Architectural Diagram (Shows how key parts of the system work)>

<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service

2. **Clone the GitHub repository in your Azure Cloud**
```bash  
git clone git@github.com:philbier/building-cicd-pipeline.git
``` 

![Git repo cloned in Azure shell](./img/git_clone_az_shell.PNG)

3. **Navigate into the cloned repo and locally test the code**   
    a. Run `make setup` to set up virtual environment  
    b. Run `source ~/.building-cicd-pipeline/bin/activate the command` to source into the virtual environment  
    c. Run `make all` to install requirements as well as run linting and testing  
You should see the following output for linting an testing

![Succesfull test of hello.py](./img/test1.PNG)

4. **Configure continuous integration with Github Actions**
The follwing screenshots shows the desired architecture where a code push from Azure Cloud shell to GitHub triggers a Github Action.

![Configure GitHub Actions](./img/configure_github_actions.png)

The cloned repository already contains the workflow `pythonapp.yml`. You should find the workflow when clicking on the Actions tab within the main view of your GitHub repository. Test the workflow by making a small change (f.e. to the README file) and check the workflow run afterwards. Your run should look be successful and look like this.

![GitHub Actions UI - Succesful build](./img/github_actions_ui.PNG)




* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


