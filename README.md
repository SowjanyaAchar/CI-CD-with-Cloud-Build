# CI-CD-with-Cloud-Build

## CI/CD with GCP Cloud Build: 

Cloud Build is a managed service that allows you to continuously build, test and deploy on Google Cloud Platform infrastructure.
Let's start with a brief introduction to CI/CD and learn about its benefits.

## What is CI/CD?

Continuous Integration  (CI ) a powerful way to continuously build and test your code. Whenever there is a change or update in the Source Code Manager like GitHub, Bitbucket etc, CI process is triggered which then builds your application and runs all the associated tests against it. 

Continuous Delivery on the other hand is a way to deploy your code to the production environment/clients etc. Just like CI, this process is also triggered by an update in SCM and build scripts help push the new version of your application to the end user.

Adopting CI/CD provides us the opportunity to automate the process of building the code, running the automation test suites and verifying the results before it can be deployed. 

## What is Cloud Build?

Cloud Build is a continuous build, test, and deploy pipeline service offered by the Google Cloud Platform. 
< “Cloud Build lets you build software quickly across all languages. Get complete control over defining custom workflows for building, testing, and deploying across multiple environments such as VMs, serverless, Kubernetes, or Firebase.” — Documentation >

## Key Features of Cloud Build are: 

1) Increased build speed:
Cloud Build makes use of Google's high-CPU VMs and also helps you cache source code and bigger image files etc to improve performance and reduce build time. 

2) Automate your deployments:
It helps you create highly customizable pipeline to automate deployments. It also comes with build in integrations with GKE ( Google Kubernetes Engine), serverless cloud functions etc. 

3) Faster deployment: 
It lets you set up triggers easily, which respond to every commit to your Source repository and automatically start the build test and deploy process within minutes. 
4) Stronger privacy and security:
Cloud Build lets you manage user access, permissions and control using IAM roles which again is highly configurable.
