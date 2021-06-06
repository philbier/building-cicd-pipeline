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
The follwing diagram shows the desired architecture where a code push from Azure Cloud shell to GitHub triggers a Github Action.

![Configure GitHub Actions](./img/configure_github_actions.png)

The cloned repository already contains the workflow `pythonapp.yml`. You should find the workflow when clicking on the Actions tab within the main view of your GitHub repository. Test the workflow by making a small change (f.e. to the README file) and check the workflow run afterwards. Your run should be successful and look like this.

![GitHub Actions UI - Succesful build](./img/github_actions_ui.PNG)

5. **Configure continuous delivery pipeline on Azure DevOps**
The follwing diagram depicts the desired end state. When code changes in your GitHub repository, it will trigger an Azure pipeline that deploys Flask code as an Azure App Service. Follow these steps (please be aware that need to authenticate probably several times and for that pop ups within your browser must be enabled):
    a. Create a resource group
    b. Create a Azure Web App within that resource group
    c. Check wether you web app is working via https://<your-appservice>.azurewebsites.net/
    d. Go to your Azure DevOps Organization an create a project  
    e. Within project settings go to **Service Connections** and create one  
        Scope level: Subscription  
        Subscription: <Your subscription>  
        Resource Group: <Resource Group you created in a.>  
        Service connection name: Flask ML App Service  
    f. Go to **Pipelines** and create pipeline using the option **GitHub (YAML)**, select your repository and configure your Azure Web App with **Python to Linux Web App on Azure**
    g. Checkin your Azure Pipeline YAML file into Github
    h. Run your Azure pipeline workflow

A successful deployment should look like the following screenshot
![Azure Pipeline - Succesful deployment](./img/azure_deployment.PNG)


6. Verify prediction with `make_predict_azure_app.sh`
    a. Change the line in `make_predict_azure_app.sh` to the following
    ```
    -X POST https://<yourappname>.azurewebsites.net:$PORT/predict
    ```
    b. Commit and push the change to GitHub and check build & deployment.
    c. Run `https://<yourappname>.azurewebsites.net:$PORT/predict` in your browser

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


