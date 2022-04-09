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
<br><b> This project is a continuation of the previous project ANSIBL AND TERRAFORM, you can find them at the link </b>

https://github.com/asiamegic/ansible_with_terraform
