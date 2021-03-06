<b>CI/CD WITH AZURE DEVOPS</b>

![cicd-pipeline](https://user-images.githubusercontent.com/85096533/162590680-2391254e-83c2-4455-96bd-2dbe1fa1bc6a.gif)


<b>Azure Pipelines automatically builds and tests code projects to make them available to others. It works with just about any language or project type. Azure Pipelines combines continuous integration (CI) and continuous delivery (CD) to test and build your code and ship it to any target.
</b>
<hr>

 Project consists of using Azure Pipelines to configure a complete CI/CD pipeline for the WeightTracker application that includes building the application and deploying it into (an existent) infrastructure. As a bonus we are going to create an additional CI/CD pipeline to automate the infrastructure updates when our Terraform code changes.
 
 ![project-cicd](https://user-images.githubusercontent.com/85096533/162590747-601d8fb8-86f4-4f2c-ac4a-9b54379950cb.png)

This repository contains two files: <br>
<b> app_ci_pipeline.yml </b> - allows you to easily deploy the CI part of the project by simply importing it into azure devops, this stage allows you to carry out integration tests.

It describes steps such as:
* Installing node js on the host.
* Install npm add-ons in the project folder.
* Packaging in archive files
* Pushing files to artifact repository on azure devopss server

<b> playbook.yaml </b> - contains an ansible script that will allow you to conduct continuous si stages after setting up this part
<hr>

<b>A set of commands necessary to install and configure the AZURE DEVOPS agent that you need to run on the host: </b>
* sudo apt update
* echo yes|sudo apt install zip
* echo Y|sudo apt install ansible
* sudo apt install sshpass
* mkdir myagent && cd myagent
* wget https://vstsagentpackage.azureedge.net/agent/2.202.0/vsts-agent-linux-x64-2.202.0.tar.gz
* tar zxvf vsts-agent-linux-x64-2.202.0.tar.gz

* ./config.sh     <b> -before you start, you need to complete configurations, such as link an account, enter the PAT key, enter the name of the agent pool, enter the name of your agent and the name of the working folder on the local machine </b>
* ./run.sh        <b> -starts the agent itself after all the settings</b>

<hr>
<br><b> This project is a continuation of the previous project ANSIBL AND TERRAFORM, you can find them at the link </b>

https://github.com/asiamegic/ansible_with_terraform

<hr>
<b> CI - continuous integration </b>

![ci](https://user-images.githubusercontent.com/85096533/162591323-aae12ce8-7427-4524-a1ce-4431e4960b4f.jpg)
<hr>


<br><b>CD - continuous deployment</b>
![cd](https://user-images.githubusercontent.com/85096533/162591343-a2348b51-5a1c-4302-9d65-34a11e180ec0.jpg)

