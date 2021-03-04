# CI/CD with GCP Cloud Build: 

Cloud Build is a managed service that allows you to continuously build, test and deploy on Google Cloud Platform infrastructure.
Let's start with a brief introduction to CI/CD and learn about its benefits.

## What is CI/CD?

Continuous Integration  (CI ) is a powerful tool to continuously build and test your code. Whenever there is a change or update in the Source Code Manager like GitHub, Bitbucket etc, CI process is triggered which then builds your application and runs all the associated tests against it. 

Continuous Delivery on the other hand is a way to deploy your code to the production environment/clients etc. Just like CI, this process is also triggered by an update in SCM and build scripts help push the new version of your application to the end user.
Adopting CI/CD provides us the opportunity to automate the process of building the code, running the automation test suites and verifying the results before it can be deployed. 

## What is Cloud Build?
Cloud Build is a continuous build, test, and deploy pipeline service offered by the Google Cloud Platform. 

> “Cloud Build lets you build software quickly across all languages. Get complete control over defining custom workflows for building, testing, and deploying across multiple environments such as VMs, serverless, Kubernetes, or Firebase.” [https://cloud.google.com/build]

## Key Features of Cloud Build are: 

1) Increased build speed:
    Cloud Build makes use of Google's high-CPU VMs and also helps you cache source code and bigger image files etc to improve performance and reduce build time. 

2) Automate your deployments:
    It helps you create a highly customizable pipeline to automate deployments. It also comes with built- in integrations with GKE ( Google Kubernetes Engine), serverless cloud functions etc. 

3) Faster deployment: 
    It lets you set up triggers easily, which respond to every commit to your Source repository and automatically start the build test and deploy process within minutes. 

4) Stronger privacy and security:
    Cloud Build lets you manage user access, permissions and control using IAM roles which again is highly configurable.

## Cloud Build Execution:

> Cloud Build executes your build as a series of build steps, where each build step is run in a Docker container. Executing build steps is analogous to executing commands in a script. - [https://cloud.google.com/build/docs]

To create a build pipeline, we need to create a build configuration file typically in YAML or JSON format which instructs the Cloud Build to perform various tasks like building artifacts when triggered. Cloud build provides a huge set of open source build tasks [https://github.com/GoogleCloudPlatform/cloud-builders]  that can be used in the configuration file or we can create our own build tasks depending on our use case.  

## Cloud build example use case: 

Here is an example of how the cloud build trigger and configuration file looks like in a real world application. To learn more about how to setup the triggers and build pipeline refer: [ https://cloud.google.com/docs/ci-cd ]

In the image below, we see a News API trigger. 
1) When the Developer checks in the code to a GitHub repository linked to the CloudBuild trigger.
2) GitHub triggers a post-commit hook to Cloud Build.
3) Cloud Build builds a container image and pushes it to Google cloud container registry. 
4) Cloud Build then notifies Cloud Run to redeploy. 
5) Cloud Run pulls the latest image from the Container Registry and runs it.
**Cloud build trigger:**
    <img src=https://github.com/SowjanyaAchar/CI-CD-with-Cloud-Build/blob/main/trigger.png width= 800 /><br>


The build configuration file for the NewAPI: 
**cloudbuild.yaml**
    <img src=https://github.com/SowjanyaAchar/CI-CD-with-Cloud-Build/blob/main/cloudbuild.png width= 500 /><br>


## References:
1) https://medium.com/swlh/how-to-ci-cd-on-google-cloud-platform-1e631cded335
2) https://medium.com/serverlessguru/serverless-ci-cd-cloud-build-e8c09e9a1018
3) https://cloud.google.com/build/docs/overview
4) 
